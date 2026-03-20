# i2r-05 CLAUDE.md
# Claude AI 전용 개발 도우미 — i2r-05 보드 전체 가이드
#
# ✅ 사용법 (claude.ai 채팅창에 아래처럼 입력):
#
#   "https://raw.githubusercontent.com/kdi6033/i2r-05/main/CLAUDE.md
#    읽고 [원하는 동작] 만들어줘"
#
# 예시:
#   "온도 30도 넘으면 LED 켜줘"
#   "스위치 누르면 부저 울려줘"
#   "WiFi 연결하고 MQTT로 센서 데이터 보내줘"

---

## 1. 보드 정보

- 보드명: i2r-05 (Arduino AI IoT Board)
- MCU: ESP32-S3-WROOM-1-N16R8
- CPU: 듀얼코어 Xtensa LX7, 최대 240MHz
- Flash: 16MB / PSRAM: 8MB
- 무선: Wi-Fi 802.11 b/g/n (2.4GHz), Bluetooth 5.0 LE
- AI: TensorFlow Lite, Vector Extension 지원
- 인증: KC 전파인증 완료
- 공식사이트: https://i2r.link
- 구매: https://i2r.link/products
- GitHub: https://github.com/kdi6033/i2r-05
- YouTube: https://www.youtube.com/@i2r-link

---

## 2. Arduino IDE 보드 설정 (필수)

```
툴 → 보드 → ESP32S3 Dev Module
Flash Size: 16MB (128Mb)
Partition Scheme: Custom
PSRAM: OPI PSRAM
Upload Speed: 921600
USB CDC On Boot: Enabled
```

### 파티션 테이블 (partitions.csv)
```csv
# Name,   Type, SubType, Offset,   Size
nvs,      data, nvs,     0x9000,   0x5000
otadata,  data, ota,     0xe000,   0x2000
app0,     app,  ota_0,   0x10000,  0x600000
app1,     app,  ota_1,   0x610000, 0x600000
coredump, data, coredump,0xC10000, 0x10000
spiffs,   data, spiffs,  0xC20000, 0x3D0000
```

---

## 3. i2r-05 기본 보드 핀맵

| 기능 | GPIO | 설명 |
|------|------|------|
| SCL (I2C) | IO17 | I2C 클럭 |
| SDA (I2C) | IO18 | I2C 데이터 |
| FR_SW | IO45 | 기능 스위치 |
| LED_RGB | IO48 | 내장 RGB LED (FastLED) |
| TX_USB | IO43 | USB TX |
| RX_USB | IO44 | USB RX |

---

## 4. Shield V1 핀맵 (학습용 확장보드)

| 기능 | GPIO | 입출력 | 비고 |
|------|------|--------|------|
| LED1 (파랑) | 47 | OUTPUT | LOW=ON |
| LED2 (빨강) | 38 | OUTPUT | LOW=ON |
| SW1 | 8 | INPUT_PULLUP | LOW=눌림 |
| SW2 | 9 | INPUT_PULLUP | LOW=눌림 |
| Rotation (가변저항) | 1 | ANALOG IN | 0~4095 |
| Buzzer | 11 | OUTPUT | tone() 사용 |
| Light (조도센서) | 2 | ANALOG IN | 0=밝음 |
| DHT11 (온습도) | 10 | DIGITAL | DHT 라이브러리 |
| LM35 (온도) | 4 | ANALOG IN | 라이브러리 불필요 |
| RGB LED Red | 15 | OUTPUT | PWM |
| RGB LED Green | 21 | OUTPUT | PWM |
| RGB LED Blue | 16 | OUTPUT | PWM |
| IR Receiver | 12 | DIGITAL IN | IRremote 라이브러리 |
| 내장 RGB LED | 48 | OUTPUT | FastLED 라이브러리 |

---

## 5. 필수 라이브러리

| 라이브러리 | 라이브러리 매니저 검색어 | 용도 |
|-----------|----------------------|------|
| DHT sensor library | DHT sensor library | DHT11 온습도 |
| FastLED | FastLED | 내장 RGB LED (48번) |
| IRremote | IRremote | IR 수신기 |
| PubSubClient | PubSubClient | MQTT 통신 |
| ArduinoJson | ArduinoJson | JSON 처리 |
| ESP32Servo | ESP32Servo | 서보모터 |

> 설치: Arduino IDE → 스케치 → 라이브러리 포함하기 → 라이브러리 관리

---

## 6. 섹션별 완성 코드

### 6-1. 내장 RGB LED (48번, FastLED)

```cpp
#include <FastLED.h>
#define LED_PIN  48
#define NUM_LEDS 1
CRGB leds[NUM_LEDS];

void setup() {
  FastLED.addLeds<WS2812B, LED_PIN, GRB>(leds, NUM_LEDS);
  FastLED.clear(); FastLED.show();
}

void loop() {
  leds[0] = CRGB::Red;   FastLED.show(); delay(500);
  leds[0] = CRGB::Green; FastLED.show(); delay(500);
  leds[0] = CRGB::Blue;  FastLED.show(); delay(500);
  leds[0] = CRGB::Black; FastLED.show(); delay(500);
  // ★ 사용자 로직 추가 구역
}
```

### 6-2. LED 제어 (47, 38번)

```cpp
#define LED1 47  // 파랑 (LOW=ON)
#define LED2 38  // 빨강 (LOW=ON)

void setup() {
  pinMode(LED1, OUTPUT); digitalWrite(LED1, HIGH);
  pinMode(LED2, OUTPUT); digitalWrite(LED2, HIGH);
}

void loop() {
  digitalWrite(LED1, LOW);  delay(1000);
  digitalWrite(LED1, HIGH); delay(1000);
  // ★ 사용자 로직 추가 구역
}
```

### 6-3. WiFi 연결 + LED 상태 표시

```cpp
#include <WiFi.h>
const char* ssid     = "YOUR_WIFI_SSID"; // ★ 수정
const char* password = "YOUR_WIFI_PW";   // ★ 수정
#define LED1 47  // 파랑
#define LED2 38  // 빨강

void setup() {
  Serial.begin(115200);
  pinMode(LED1, OUTPUT); digitalWrite(LED1, HIGH);
  pinMode(LED2, OUTPUT); digitalWrite(LED2, LOW); // 빨강=연결중
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) { delay(500); }
  Serial.println("✅ WiFi: " + WiFi.localIP().toString());
  digitalWrite(LED2, HIGH); // 빨강 OFF
  digitalWrite(LED1, LOW);  // 파랑=연결완료
}

void loop() {
  // ★ 사용자 로직 추가 구역
}
```

### 6-4. 스위치 입력 (8, 9번)

```cpp
#define SW1 8
#define SW2 9

void setup() {
  Serial.begin(115200);
  pinMode(SW1, INPUT_PULLUP);
  pinMode(SW2, INPUT_PULLUP);
}

void loop() {
  if (digitalRead(SW1) == LOW) { Serial.println("SW1 눌림"); delay(200); }
  if (digitalRead(SW2) == LOW) { Serial.println("SW2 눌림"); delay(200); }
  // ★ 사용자 로직 추가 구역
}
```

### 6-5. 가변저항 (1번)

```cpp
#define ROT_PIN 1

void setup() {
  Serial.begin(115200);
  analogReadResolution(12);
}

void loop() {
  int value = analogRead(ROT_PIN); // 0~4095
  Serial.print("가변저항: "); Serial.println(value);
  delay(500);
  // ★ 사용자 로직 추가 구역
}
```

### 6-6. 부저 (11번)

```cpp
#define BUZZER 11
#define DO 262
#define RE 294
#define MI 330
#define FA 349
#define SOL 392
#define LA 440
#define SI 494

int melody[]   = {DO,DO,SOL,SOL,LA,LA,SOL, FA,FA,MI,MI,RE,RE,DO};
int duration[] = {4, 4, 4,  4,  4, 4, 2,   4, 4, 4, 4, 4, 4, 2};

void setup() { pinMode(BUZZER, OUTPUT); }

void loop() {
  for (int i = 0; i < 14; i++) {
    int dur = 1000 / duration[i];
    tone(BUZZER, melody[i], dur);
    delay(dur * 1.3);
    noTone(BUZZER);
  }
  delay(2000);
  // ★ 사용자 로직 추가 구역
}
```

### 6-7. 조도 센서 (2번)

```cpp
#define LIGHT_PIN 2

void setup() {
  Serial.begin(115200);
  analogReadResolution(12);
}

void loop() {
  int light = analogRead(LIGHT_PIN); // 0=밝음, 4095=어두움
  Serial.print("조도: "); Serial.println(light);
  delay(500);
  // ★ 사용자 로직 추가 구역
}
```

### 6-8. DHT11 온습도 (10번)

```cpp
#include "DHT.h"
#define DHTPIN  10
#define DHTTYPE DHT11
DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(115200);
  dht.begin();
}

void loop() {
  float humi = dht.readHumidity();
  float temp = dht.readTemperature();
  if (isnan(humi) || isnan(temp)) { Serial.println("❌ 센서 오류"); delay(2000); return; }
  Serial.print("온도: "); Serial.print(temp); Serial.println("°C");
  Serial.print("습도: "); Serial.print(humi); Serial.println("%");
  delay(2000);
  // ★ 사용자 로직 추가 구역
}
```

### 6-9. LM35 온도 센서 (4번)

```cpp
#define LM35_PIN 4

void setup() {
  Serial.begin(115200);
  analogReadResolution(12);
}

void loop() {
  int   adc  = analogRead(LM35_PIN);
  float volt = (adc / 4095.0) * 3.3;
  float temp = volt * 100.0; // 1V=100°C
  Serial.print("온도: "); Serial.print(temp, 1); Serial.println("°C");
  delay(1000);
  // ★ 사용자 로직 추가 구역
}
```

### 6-10. RGB LED (15, 21, 16번)

```cpp
#define RGB_R 15
#define RGB_G 21
#define RGB_B 16

void setRGB(int r, int g, int b) {
  analogWrite(RGB_R, r);
  analogWrite(RGB_G, g);
  analogWrite(RGB_B, b);
}

void setup() {
  pinMode(RGB_R, OUTPUT);
  pinMode(RGB_G, OUTPUT);
  pinMode(RGB_B, OUTPUT);
}

void loop() {
  setRGB(255,0,0); delay(500); // 빨강
  setRGB(0,255,0); delay(500); // 녹색
  setRGB(0,0,255); delay(500); // 파랑
  setRGB(0,0,0);   delay(500); // 끄기
  // ★ 사용자 로직 추가 구역
}
```

### 6-11. IR 수신기 (12번)

```cpp
#include <IRremote.hpp>
#define IR_PIN 12

void setup() {
  Serial.begin(115200);
  IrReceiver.begin(IR_PIN);
}

void loop() {
  if (IrReceiver.decode()) {
    Serial.print("IR: 0x");
    Serial.println(IrReceiver.decodedIRData.decodedRawData, HEX);
    IrReceiver.resume();
  }
  // ★ 사용자 로직 추가 구역
}
```

### 6-12. WiFi + MQTT 완전 연동

```cpp
#include <WiFi.h>
#include <PubSubClient.h>
#include <ArduinoJson.h>

const char* ssid        = "YOUR_WIFI_SSID"; // ★ 수정
const char* password    = "YOUR_WIFI_PW";   // ★ 수정
const char* mqtt_server = "ai.doowon.ac.kr";
const int   mqtt_port   = 1883;

WiFiClient   espClient;
PubSubClient client(espClient);
String mac;
unsigned long lastPublish = 0;

void callback(char* topic, byte* payload, unsigned int length) {
  StaticJsonDocument<256> doc;
  deserializeJson(doc, payload, length);
  // ★ MQTT 수신 처리 추가 구역
}

void reconnect() {
  while (!client.connected()) {
    if (client.connect(mac.c_str())) {
      client.subscribe(("i2r/" + mac + "/in").c_str());
      Serial.println("✅ MQTT 연결됨");
    } else { delay(5000); }
  }
}

void publishData(float temp, float humi) {
  StaticJsonDocument<256> doc;
  doc["mac"]  = mac;
  doc["temp"] = temp;
  doc["humi"] = humi;
  String payload;
  serializeJson(doc, payload);
  client.publish(("i2r/" + mac + "/out").c_str(), payload.c_str());
}

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) delay(500);
  mac = WiFi.macAddress();
  Serial.println("✅ WiFi: " + mac);
  Serial.println("📡 대시보드: https://i2r.link/device/" + mac);
  client.setServer(mqtt_server, mqtt_port);
  client.setCallback(callback);
  // ★ 초기화 추가 구역
}

void loop() {
  if (!client.connected()) reconnect();
  client.loop();
  if (millis() - lastPublish > 5000) {
    lastPublish = millis();
    // ★ 센서 읽기 및 publishData() 호출 구역
  }
}
```

### 6-13. 서보모터 MQTT 제어

```cpp
#include <WiFi.h>
#include <PubSubClient.h>
#include <ArduinoJson.h>
#include <ESP32Servo.h>

const char* ssid        = "YOUR_WIFI_SSID"; // ★ 수정
const char* password    = "YOUR_WIFI_PW";   // ★ 수정
const char* mqtt_server = "ai.doowon.ac.kr";
const int   mqtt_port   = 1883;
const int   servoPin    = 6;

Servo servo;
WiFiClient espClient;
PubSubClient client(espClient);
String mac;

void controlServo(int order) {
  if      (order == 1) servo.writeMicroseconds(1800); // 전진
  else if (order == 2) servo.writeMicroseconds(1200); // 후진
  else                 servo.writeMicroseconds(1500); // 정지
}

void callback(char* topic, byte* payload, unsigned int length) {
  StaticJsonDocument<256> doc;
  deserializeJson(doc, payload, length);
  controlServo(doc["order"]);
}

void setup() {
  Serial.begin(115200);
  servo.attach(servoPin);
  servo.writeMicroseconds(1500);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) delay(500);
  mac = WiFi.macAddress();
  client.setServer(mqtt_server, mqtt_port);
  client.setCallback(callback);
}

void loop() {
  if (!client.connected()) {
    if (client.connect(mac.c_str()))
      client.subscribe(("i2r/" + mac + "/in").c_str());
  }
  client.loop();
}
```

---

## 7. Claude 응답 규칙

사용자 요청을 받으면 반드시 아래 형식으로 답한다.

### ✅ 완성 코드
(검증된 베이스 코드 기반, ★ 구역에만 추가, Arduino IDE 바로 업로드 가능)

### 📌 수정된 부분
| 위치 | 수정 내용 |
|------|----------|
| (위치) | (내용) |

### 🔧 Arduino IDE 업로드 순서
1. Arduino IDE 열기
2. 완성 코드 전체 복사 → 붙여넣기
3. 툴 → 보드 → ESP32S3 Dev Module 선택
4. 툴 → 포트 → COM 포트 선택
5. ➡️ 업로드 클릭
6. 시리얼 모니터 115200으로 확인
7. MQTT 연동 시 https://i2r.link/device/{MAC} 대시보드 확인

### ❓ 오류 해결표
| 오류 | 해결 |
|------|------|
| DHT.h not found | 라이브러리 매니저 → DHT sensor library 설치 |
| FastLED.h not found | 라이브러리 매니저 → FastLED 설치 |
| IRremote.hpp not found | 라이브러리 매니저 → IRremote 설치 |
| PubSubClient.h not found | 라이브러리 매니저 → PubSubClient 설치 |
| ArduinoJson.h not found | 라이브러리 매니저 → ArduinoJson 설치 |
| 업로드 실패 | BOOT 버튼 누른 채 업로드 클릭 |
| 포트 인식 안됨 | 데이터 전송 가능 USB 케이블로 교체 |
| WiFi 연결 안됨 | 2.4GHz 확인 (5GHz 불가) |
| MQTT 연결 안됨 | 브로커 ai.doowon.ac.kr, 포트 1883 확인 |

---

## 8. 사용 예시

```
기초:
"LED1 LED2 1초 간격으로 교차 점등해줘"
"SW1 누르면 LED1 켜고 SW2 누르면 꺼줘"
"가변저항 값에 따라 내장 RGB LED 색상 바꿔줘"
"부저로 학교종 연주해줘"

센서 응용:
"DHT11 온도 30도 넘으면 빨간 LED 켜고 부저 울려줘"
"LM35 온도 1초마다 시리얼로 출력해줘"
"조도 센서 어두우면 파란 LED 켜줘"
"IR 리모컨 버튼 누르면 LED 토글해줘"

WiFi/MQTT:
"WiFi 연결하고 DHT11 데이터를 MQTT로 보내줘"
"MQTT로 LED 원격 제어하고 i2r.link에서 확인하게 해줘"
"서보모터를 MQTT로 전진/후진/정지 제어해줘"

복합:
"모든 센서 값을 5초마다 MQTT로 보내줘"
"온도 30도 넘으면 자동으로 부저 울리고 MQTT로 알림 보내줘"
```
