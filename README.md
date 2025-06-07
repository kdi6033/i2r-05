# i2r-05 AI IoT 아두이노 보드 (KC 전파인증)

아래 소스코드를 보드에 설치하면 자동으로 사이트에 보드가 등록되고 모니터링 할 수 있습니다. 이러한 프로그램을 실현 할 수 있게 AI를 활용해 프로그램 과정을 이 사이트에서 설명 하겠습니다.

[아두이노 소스프로그램 링크](https://github.com/kdi6033/i2r-05/blob/main/file/board-i2r-05.ino)  

[![26-1 ESP32-S3 아두이노 실습보드 전파인증](https://img.youtube.com/vi/buiv6945OOA/0.jpg)](https://youtu.be/buiv6945OOA) 

콘트롤 사이트 로그인 : https://ai.doowon.ac.kr 

보드는 블루투스와 와이파이 통신을 가지고 있습니다.    
- 블루투스 : 와이파이 정보를 입력하는데 사용, 스마트폰의 블루투스 이용    
- 와이파이 : 와이파이를 이용해 mqtt 프로토콜 통신으로 보드를 모니터링하고 제어 한다. 콘트롤 사이트 접속해서 제어    


# 개요
GitHub의 i2r-05 레포지터리를 기반으로 학생들에게 IoT 및 임베디드 시스템을 교육합니다. 여기서는 i2r-05 보드를 활용하여 기본적인 하드웨어 이해부터 실습을 진행하고, On-Device AI(온디바이스 AI) 구현합니다. 그리고 스마트팜을 하시는 분들을 위해서 각종 센서와 액튜에이터를 자동으로 연결하여 스마트폰과 PC에서 모니터링/제어 할 수 있게 합니다.

# 교육 목표
- i2r-05 보드를 활용하여 하드웨어 및 펌웨어 개발의 기초를 익힘
- Wi-Fi 및 MQTT 기반의 IoT 통신을 실습하여 네트워크 프로그래밍 이해
- 머신러닝 및 On-Device AI 개념을 학습하고 실제 보드에서 실행 가능하도록 구현
- ESP32-S3의 강력한 연산 성능을 활용하여 실시간 데이터 분석 및 처리

# 교육 과정 구성
## (1) 기초 과정: i2r-05 보드 이해 및 환경 설정
- i2r-05 보드 개요 및 사양 분석
- 개발 환경 구축(Arduino IDE, ESP-IDF, PlatformIO)
- 기본적인 GPIO 제어 및 센서 연결 실습
- 시리얼 통신 및 Wi-Fi 설정
## (2) 중급 과정: IoT 및 네트워크 프로그래밍
- MQTT 프로토콜을 활용한 데이터 송수신
- 클라우드 서버(AWS, Firebase, Node.js 서버)와의 연동
- MongoDB와 연계하여 데이터 저장 및 분석
## (3) 고급 과정: On-Device AI 구현
- ESP32-S3의 AI 가속 기능(TensorFlow Lite Micro, Edge Impulse) 소개
- 간단한 머신러닝 모델(이미지 인식, 음성 인식) 학습 및 배포
- 실시간 센서 데이터를 활용한 AI 모델 적용
- 최적화 및 배터리 절약을 위한 저전력 설계

# 기대 효과
- 학생들이 IoT 및 AI 시스템의 기본 개념을 이해하고 직접 구현할 수 있도록 지원
- AI가 탑재된 임베디드 시스템을 직접 설계하고 응용할 수 있는 능력 배양
- 실제 산업 현장에서 활용 가능한 IoT 및 AI 기술 습득

ESP32 S3 16M Flash, AI IoT 개발용 보드
![i2r-05](https://github.com/user-attachments/assets/4ba415d9-08e6-4b2c-9396-1d3f35ffdfe2)
![i2r-05 회로도](https://github.com/user-attachments/assets/ed673ea3-f054-4370-ae92-979a29e72c4d)

# ESP32-S3-WROOM-1-N16R8 설명
ESP32-S3-WROOM-1-N16R8은 Espressif Systems에서 개발한 고성능 Wi-Fi 및 Bluetooth LE 모듈입니다. 이 모듈은 ESP32-S3 SoC를 기반으로 하며, **16MB의 플래시 메모리(N16)와 8MB의 PSRAM(R8)**을 탑재하고 있습니다.

### 1. 주요 특징
#### (1) CPU 및 성능
- 듀얼코어 Xtensa® LX7 32비트 프로세서
- 최대 240MHz 클럭 속도
- AI 및 DSP 기능 향상 (벡터 연산 가속 지원)
#### (2) 메모리
- 16MB 플래시 메모리 (N16)
- 8MB PSRAM (R8) → AI, 이미지 처리, 데이터 버퍼링에 유용
#### (3)무선 기능
- Wi-Fi 802.11 b/g/n (2.4GHz)
- Bluetooth 5.0 LE (Low Energy)
- WPA3 보안 지원
#### (4) USB 기능
- Full-Speed USB OTG (USB 1.1)
- USB CDC/JTAG 디버깅 지원
- USB-Serial 통신 가능 (UART 필요 없음)
#### (5) GPIO 및 확장성
- 최대 45개의 GPIO 핀 제공
- SPI, I2C, UART, PWM, ADC, DAC 지원
- JTAG 디버깅 지원
#### (6) 저전력 설계
- Deep Sleep 모드에서 μA 단위의 전력 소모
- ULP (Ultra-Low Power) 코프로세서 내장
#### (7) AI 및 머신러닝
- Vector Extension (AI 가속기) 포함
- TensorFlow Lite, ESP-DSP 최적화 지원

### 2. ESP32-S3-WROOM-1-N16R8의 장점
- 대용량 PSRAM (8MB) 탑재 : 이미지 처리, AI 모델, 오디오 스트리밍 등에 적합
- Wi-Fi + Bluetooth 동시 지원 : BLE를 활용한 IoT 기기 및 스마트 디바이스 개발 가능
- USB OTG 지원 : 직접 USB 장치와 통신 가능 (키보드, 마우스, 스토리지 연결)
- 보안 기능 강화 : Secure Boot, Flash Encryption, AES-XTS 암호화 지원
- ESP-IDF 및 Arduino 지원 : ESP-IDF, Arduino, MicroPython 등 다양한 개발 환경 제공

### 3. ESP32-S3-WROOM-1-N16R8의 활용 사례
- AI 및 머신러닝
- 온디바이스 AI (On-Device AI)
- 얼굴 인식, 음성 인식, AIoT (AI + IoT)
- IoT 및 스마트 디바이스
- Wi-Fi 기반 스마트 홈 시스템
- BLE 센서 네트워크
- 임베디드 시스템 개발
- USB 기반 주변기기 개발
- 드론, 로봇 제어 시스템
- 실시간 데이터 처리
- MQTT 및 WebSocket을 활용한 실시간 데이터 전송
- 센서 데이터를 클라우드로 전송하여 모니터링

### 4. ESP32-S3-WROOM-1-N16R8 개발 환경
- ESP-IDF (Espressif 공식 SDK)
- Arduino IDE
- Visual Code
- PlatformIO
- MicroPython
- FreeRTOS 기반 멀티태스킹 지원

arduino IDE를 사용하여 컴파일 하려면 tool 에서 보드설정은 아래와 같습니다.
<img width="300" src="https://github.com/user-attachments/assets/786d4d17-e62d-4c16-bae7-ef9bf459cffe" />    


# 1. ESP32 블루투스(BLE) 통신 개요 및 실습
ESP32는 Bluetooth Classic과 Bluetooth Low Energy(BLE)를 모두 지원하는 강력한 무선 모듈입니다.
BLE는 저전력으로 데이터를 전송할 수 있어, IoT(사물인터넷) 기기에서 널리 사용됩니다.
블루투스는 스마트폰의 블루투스와 연결하여 와이파이 정보를 보드로 전송하여 통신 접속을 하게 합니다. 

[📺 영상 보기- AI IoT 아두이노 보드 와이파이, 크라우드 연결](https://youtu.be/R9wEoO4aQpU)

## 🔗 [📺 영상 보기 - **AI IoT 아두이노 보드 와이파이, 크라우드 연결**](https://youtu.be/R9wEoO4aQpU)

> 🧠 이 영상에서는 **i2r-05 AI IoT 보드**를 Wi-Fi 및 클라우드에 연결하는 방법을 자세히 설명합니다.
> - 📡 와이파이 설정 방법
> - ☁️ 크라우드 연동 방법
> - 📱 웹앱 접속 및 제어 방법

## 🔗 [📺 영상 보기 - **AI IoT 아두이노 보드 웹앱 사용법**](https://youtu.be/R9wEoO4aQpU)

> 크라우드에 접속하여 스위치, 온도, 습도, 아나로그 센서, 조도센서 등을 원격으로 모니터링 제어 하는 방법을 소개한다.


## 보드의 RGB Led 제어 (48번핀)
보드에는 RGB Led가 48번으로 장착되었습니다. 다음은 색상을 제어하는 프로그램 입니다.    

## 🔗 [📺 영상 보기 - **AI IoT 아두이노 보드  RGB Led 제어 (48번핀)**](https://youtu.be/dB-iA1lIVrQ)

> 보드에는 RGB Led가 48번으로 장착되었습니다.  이 Led의 색상을 제어하는 프로그램 입니다.
> 무지게, 점멸,흐름 효과 프로그램

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="RGB Led" width="100">  48번 RGB Led 제어    
```
esp32 s3 를 사용하고 48번핀에 RGB Led  가 연결되 있습니다. 이 한선으로 칼라를 제어 합니다. 빨강 파랑 녹색 불들어오게 프로그램 해줘
```
아두이노 프로그램
```
#include <Adafruit_NeoPixel.h>

#define LED_PIN 48      // RGB LED가 연결된 핀 번호
#define NUM_PIXELS 1    // 제어할 LED 개수

Adafruit_NeoPixel strip(NUM_PIXELS, LED_PIN, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.begin();         // LED 제어를 위한 초기화
  strip.show();          // LED를 초기화 상태로 설정
}

void loop() {
  setColor(255, 0, 0);   // 빨강색
  delay(1000);           // 1초 대기
  setColor(0, 255, 0);   // 녹색
  delay(1000);           // 1초 대기
  setColor(0, 0, 255);   // 파랑색
  delay(1000);           // 1초 대기
}

// RGB 색상 설정 함수
void setColor(uint8_t red, uint8_t green, uint8_t blue) {
  strip.setPixelColor(0, strip.Color(red, green, blue)); // 첫 번째 LED의 색상 설정
  strip.show();                                         // 설정한 색상을 출력
}
```

Adafruit_NeoPixel 는 내부에 인터럽트를 사용하여 I2c와 충돌이 일어 나서 제어용 프로그램과 함깨 구성하면 에러가 자주 발생하여 FastLED.h 를 사용해서 Led를 제어 합니다.   
이는 I2C와 충돌이 일어 날 수 있으나 앞에 프로그램 보다는 효율적 입니다.    
다음은 무지개 효과, 점멸, 밝기를 조절하는 프로그램 입니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="RGB Led" width="100">  무지게, 점멸,흐름 효과 프로그램    
```
esp32 s3 를 사용하고 48번핀에 RGB Led  가 연결되 있습니다. FastLED.h를 이용해서 무지게, 점멸,흐름 효과 프로그램 해줘
```
```
#include <FastLED.h>

#define NUM_LEDS 1         // LED 개수 (1개)
#define DATA_PIN 48        // 데이터 핀 (GPIO 48 고정)
#define LED_TYPE WS2812B   // LED 종류
#define COLOR_ORDER GRB    // 색 순서

CRGB leds[NUM_LEDS];
uint8_t gHue = 0;          // 색상 변화용 변수

void setup() {
  FastLED.addLeds<LED_TYPE, DATA_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.clear();
  FastLED.show();
}

void loop() {
  rainbowEffect();   // 🌈 무지개 효과
  blinkEffect();     // ✨ 점멸 효과
  flowingEffect();   // 💨 흐름 효과 (1개 LED용으로 동작)
}

// 🌈 무지개 효과 (1개 LED 색상 부드럽게 변화)
void rainbowEffect() {
  for (int i = 0; i < 100; i++) {
    leds[0] = CHSV(gHue++, 255, 255); // 색상 변화
    FastLED.show();
    delay(50);
  }
}

// ✨ 점멸 효과 (흰색으로 깜빡임)
void blinkEffect() {
  for (int i = 0; i < 5; i++) {
    leds[0] = CRGB::White;
    //leds[0] = CRGB(255, 255, 255);
    FastLED.show();
    delay(300);

    leds[0] = CRGB::Black;
    //leds[0] = CRGB(0, 0, 0);
    FastLED.show();
    delay(300);
  }
}

// 💨 흐름 효과 (1개 LED만 사용하여 밝기 변화 느낌)
void flowingEffect() {
  // 밝기가 점점 밝아졌다가 어두워지는 흐름 효과
  for (int b = 0; b <= 255; b += 5) {
    leds[0] = CHSV(gHue, 255, b);
    FastLED.show();
    delay(20);
  }
  for (int b = 255; b >= 0; b -= 5) {
    leds[0] = CHSV(gHue, 255, b);
    FastLED.show();
    delay(20);
  }
}
```

# 1. i2r-05 Shield V1 보드
<img width="482" alt="i2r Shield V1" src="https://github.com/user-attachments/assets/fcc54b19-4a71-4e17-8461-90e9ae864907" />    

 Arduino 기반의 다목적 학습 보드로, 추가적인 납땜이나 복잡한 배선 없이 다양한 실험을 수행할 수 있습니다. 보드에 내장된 다양한 모듈을 활용하여, 코드를 다운로드하는 것만으로 실험을 완료할 수 있도록 설계되었습니다.
 
| i2r-05 | name | 설명 |
|--------|-------|-------|
| 47 | LED1 D13 파랑 | 여러 개의 LED가 포함되어 있어 디지털 출력 실험 가능 |
| 38 | LED2 D12 빨강 | 여러 개의 LED가 포함되어 있어 디지털 출력 실험 가능 |
| 8 | SW1 D2 | 입력 실험을 위한 버튼 제공 |
| 9 | SW2 D3 | 입력 실험을 위한 버튼 제공 |
| 1 | Rotation A0 | 가변 저항을 이용한 아날로그 입력 실험 가능 |
| 11 | Buzzer D5 | 소리를 내는 장치로, 알람 및 음향 실험 가능 |
| 2 | Light A1 | 조도 센서를 이용한 빛 감지 실험 가능 |
| 10 | DHT11 D4 | 	온도 측정 실험 가능 |
| 4  | LM35 A2 | 	온도 측정 실험 가능 |
| 15 | RGB LED red | 빨간색 Led 입력 핀 |
| 21 | RGB LED green | 녹색 Led 입력 핀 |
| 16 | RGB LED blue | 파란색 Led 입력 핀 |
| 12 | IR Receiver D6 | 	적외선 리모컨을 이용한 제어 가능 |


## 1.2 Led 제어 (47, 38 번핀)
ESP32-S3 보드의 47번 핀과 38번 핀에 연결된 LED를 1초 간격으로 교차로 점등하는 Arduino 프로그램입니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="Led Control" width="100">  47, 38번 Led 제어    
```
esp32 s3 보드 47, 38번 핀에 led가 연결되어 있습니다. 1초 간격으로 교차로 점등하게 프록램 해줘요
```
아두이노 프로그램
```
#define LED1_PIN 47 // 첫 번째 LED 핀 번호
#define LED2_PIN 38 // 두 번째 LED 핀 번호

void setup() {
  pinMode(LED1_PIN, OUTPUT); // LED1 핀을 출력 모드로 설정
  pinMode(LED2_PIN, OUTPUT); // LED2 핀을 출력 모드로 설정

  digitalWrite(LED1_PIN, LOW); // LED1 초기 상태 꺼짐
  digitalWrite(LED2_PIN, LOW); // LED2 초기 상태 꺼짐
}

void loop() {
  digitalWrite(LED1_PIN, HIGH); // LED1 켜기
  digitalWrite(LED2_PIN, LOW);  // LED2 끄기
  delay(1000);                 // 1초 대기

  digitalWrite(LED1_PIN, LOW); // LED1 끄기
  digitalWrite(LED2_PIN, HIGH); // LED2 켜기
  delay(1000);                 // 1초 대기
}
```

## 1.3 스위치 입력 (8, 9 번핀)
ESP32-S3 보드의 8번 핀과 9번 핀에 연결된 스위치를 감지하고, 스위치를 누를 때마다 시리얼 포트로 해당 상태를 출력하는 Arduino 프로그램입니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="Switch Input" width="100">  8,9번 스위치 입력    
```
esp32 s3 보드 8,9 번핀에 스위치가 연결되어 있습니다. 스위치를 누르면 시리얼포트로 이를 알려줘
```
아두이노 프로그램
```
#define SWITCH1_PIN 8  // 첫 번째 스위치 핀 번호
#define SWITCH2_PIN 9  // 두 번째 스위치 핀 번호

void setup() {
  Serial.begin(115200);              // 시리얼 통신 초기화
  pinMode(SWITCH1_PIN, INPUT_PULLUP); // 스위치1 핀을 입력 모드로 설정 및 내부 풀업 저항 활성화
  pinMode(SWITCH2_PIN, INPUT_PULLUP); // 스위치2 핀을 입력 모드로 설정 및 내부 풀업 저항 활성화
}

void loop() {
  if (digitalRead(SWITCH1_PIN) == LOW) { // 스위치1이 눌렸을 때 (풀업 상태에서 LOW)
    Serial.println("Switch 1 Pressed");
    delay(200); // debounce 방지를 위한 딜레이
  }
  if (digitalRead(SWITCH2_PIN) == LOW) { // 스위치2가 눌렸을 때 (풀업 상태에서 LOW)
    Serial.println("Switch 2 Pressed");
    delay(200); // debounce 방지를 위한 딜레이
  }
}
```

## 1.4 아나로그 입력 (1 번핀)
ESP32-S3 보드의 1번 핀에 아날로그 입력이 연결하여 해당 값을 읽어서 시리얼 포트로 출력하는 Arduino 프로그램입니다.
<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="Analog Input" width="100">  1번 아나로그 입력    
```
esp32 s3 보드 1 번핀에 아나로그 입력이 연결되어 있습니다. 입력 값을 시리얼포트로 알려줘
```
- ANALOG_PIN은 1번 핀으로 설정하여 ADC1 채널을 사용합니다.
- analogReadResolution(12)를 사용하여 아날로그 입력 값을 **12비트 해상도(0 ~ 4095)**로 읽습니다. 기본값은 12비트입니다.
- analogRead(ANALOG_PIN) 함수로 아날로그 값을 읽습니다. 읽은 값은 0에서 4095 범위의 정수로 반환됩니다.
- 
아두이노 프로그램
```
#define ANALOG_PIN 1  // 아날로그 입력 핀 번호

void setup() {
  Serial.begin(115200);       // 시리얼 통신 초기화
  analogReadResolution(12);   // 12비트 해상도 설정 (0 ~ 4095)
}

void loop() {
  int analogValue = analogRead(ANALOG_PIN);  // 아날로그 값 읽기
  Serial.print("Analog Value: ");
  Serial.println(analogValue);              // 값을 시리얼로 출력
  delay(500);                               // 500ms 대기
}
```

## 1.5 Buzzer 출력 (11 번핀)

ESP32-S3 보드의 11번 핀에 연결된 부저를 제어하기 위해 Arduino 코드를 작성했습니다. 부저는 PWM 신호를 통해 제어되며, 이를 통해 다양한 음을 생성할 수 있습니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="Buzzer 출력" width="100">  11번 Buzzer 출력    
```
esp32 s3 보드 11 번핀에 Buzzer가 연결되어 있습니다. 출력이 나오게 프로그램해줘
```
아두이노 프로그램
```
#define ANALOG_PIN 1  // 아날로그 입력 핀 번호

void setup() {
  Serial.begin(115200);       // 시리얼 통신 초기화
  analogReadResolution(12);   // 12비트 해상도 설정 (0 ~ 4095)
}

void loop() {
  int analogValue = analogRead(ANALOG_PIN);  // 아날로그 값 읽기
  Serial.print("Analog Value: ");
  Serial.println(analogValue);              // 값을 시리얼로 출력
  delay(500);                               // 500ms 대기
}
```
<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="음악연주" width="100">  음악연주   
```
부져로 음악연주하는 프로그램 만들어줘
```
ESP32-S3의 부저를 사용해 간단한 음악을 연주하는 프로그램을 작성할 수 있습니다. 아래는 아두이노의 tone() 함수를 사용하여 **"Twinkle Twinkle Little Star"**를 연주하는 예제입니다. 
```
#define BUZZER_PIN 11  // 부저가 연결된 핀 번호

// 음계의 주파수 정의 (도, 레, 미, 파, 솔, 라, 시)
#define NOTE_C4  262
#define NOTE_D4  294
#define NOTE_E4  330
#define NOTE_F4  349
#define NOTE_G4  392
#define NOTE_A4  440
#define NOTE_B4  494
#define NOTE_C5  523

// 멜로디 음계 배열
int melody[] = {
  NOTE_C4, NOTE_C4, NOTE_G4, NOTE_G4, NOTE_A4, NOTE_A4, NOTE_G4,
  NOTE_F4, NOTE_F4, NOTE_E4, NOTE_E4, NOTE_D4, NOTE_D4, NOTE_C4
};

// 각 음계의 지속 시간 (4분의 1, 8분의 1 등)
int noteDurations[] = {
  4, 4, 4, 4, 4, 4, 2,
  4, 4, 4, 4, 4, 4, 2
};

void setup() {
  pinMode(BUZZER_PIN, OUTPUT); // 부저 핀을 출력 모드로 설정
}

void loop() {
  // 멜로디 재생
  for (int i = 0; i < sizeof(melody) / sizeof(melody[0]); i++) {
    int noteDuration = 1000 / noteDurations[i];  // 음 길이 계산
    tone(BUZZER_PIN, melody[i], noteDuration);   // 음 출력
    delay(noteDuration * 1.3);                   // 음 사이 간격 (지속 시간의 30% 추가)
    noTone(BUZZER_PIN);                          // 음 끄기
  }

  delay(2000); // 전체 멜로디 끝난 후 2초 대기
}
```

## 1.6 Light 센서 (2 번핀)

ESP32-S3 보드의 11번 핀에 연결된 부저를 제어하기 위해 Arduino 코드를 작성했습니다. 부저는 PWM 신호를 통해 제어되며, 이를 통해 다양한 음을 생성할 수 있습니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="Light 센서" width="100">  Light 센서
```
sp32 s3 보드 2 번핀에 Light 센서가 연결되어 있습니다. 조도를 출력하는 프로그램해줘
```
- LIGHT_SENSOR_PIN 설정: 센서가 연결된 핀 번호를 #define으로 정의합니다.
- analogReadResolution(12): ESP32-S3의 ADC는 최대 12비트 해상도를 지원합니다. 이를 설정해 ADC 값이 0~4095 범위로 출력되도록 합니다.
- ADC 값을 전압으로 변환: 조도 센서에서 출력된 값은 ADC를 통해 읽은 뒤, 전압 값으로 변환됩니다.
계산 공식: 전압 = (ADC 값 / 최대 ADC 값) * 기준 전압
- Serial 출력: 읽은 ADC 값과 전압 값을 시리얼 모니터에 출력합니다
  
아두이노 프로그램
```
#define LIGHT_SENSOR_PIN 2  // Light 센서가 연결된 핀

void setup() {
  Serial.begin(115200);           // 시리얼 통신 초기화
  pinMode(LIGHT_SENSOR_PIN, INPUT);  // Light 센서 핀을 입력으로 설정
  analogReadResolution(12);       // 12비트 ADC 해상도 설정 (0~4095)
}

void loop() {
  int lightValue = analogRead(LIGHT_SENSOR_PIN);  // Light 센서 값 읽기
  float voltage = (lightValue / 4095.0) * 3.3;    // ADC 값을 전압으로 변환 (ESP32-S3의 기본 전압 기준은 3.3V)

  Serial.print("Light Sensor Value: ");
  Serial.print(lightValue);                       // ADC 값 출력
  Serial.print(" | Voltage: ");
  Serial.print(voltage, 2);                       // 전압 값 출력
  Serial.println(" V");

  delay(500);  // 500ms 대기
}
```

## 1.7 DHT11 온습도 센서 (10 번핀)

이 프로그램은 DHT 라이브러리를 사용하여 온도와 습도를 읽고 시리얼 모니터에 출력합니다.   

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="DHT11 온습도 센서" width="100">  DHT11 온습도 센서
```
sp32 s3 보드 10 번핀에  DHT11 온습도 센서가 연결되어 있습니다. 온습도를 출력하는 프로그램해
```
- 라이브러리 설치 : DHT sensor library by Adafruit 
- #define DHTTYPE DHT11: DHT 센서의 타입을 지정합니다.
- 데이터 읽기:
readHumidity(): 습도를 읽습니다.
readTemperature(): 온도를 읽습니다
- 출력 형식: 온도는 °C, 습도는 % 단위로 출력됩니다.
- 지연 시간: 센서의 데이터 갱신 주기(최대 2초)에 맞춰 delay(2000)을 사용하여 2초마다 값을 읽습니다.

아두이노 프로그램
```
#include "DHT.h"  //DHT sensor library by Adafruit

#define DHTPIN 10       // DHT 센서가 연결된 핀 번호
#define DHTTYPE DHT11   // 사용하는 센서의 유형 (DHT11)

// DHT 센서 객체 생성
DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(115200);  // 시리얼 통신 초기화
  dht.begin();           // DHT 센서 초기화
  Serial.println("DHT11 센서를 이용한 온습도 측정 시작");
}

void loop() {
  float humidity = dht.readHumidity();     // 습도 값 읽기
  float temperature = dht.readTemperature(); // 온도 값 읽기

  // DHT 센서 데이터 유효성 확인
  if (isnan(humidity) || isnan(temperature)) {
    Serial.println("센서로부터 데이터를 읽을 수 없습니다!");
  } else {
    Serial.print("온도: ");
    Serial.print(temperature);
    Serial.println(" °C");

    Serial.print("습도: ");
    Serial.print(humidity);
    Serial.println(" %");
  }

  delay(2000); // 2초마다 측정
}
```

## 1.8 LM35 온도 센서 (4 번핀)

LM35 온도 센서는 아날로그 출력 타입의 온도 센서입니다. 온도를 섭씨(°C)로 측정하며, 출력 전압은 섭씨 1도당 10mV입니다. 이를 ESP32-S3의 4번 핀에 연결하여 값을 읽고 온도를 출력하는 프로그램은 다음과 같이 작성할 수 있습니다.

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="LM35 온도 센서" width="100">  LM35 온도 센서
```
LM35 센서가 4번핀에 연결되어 있어요 프로그램 해주세요
```
아두이노 프로그램
```
#define LM35_PIN 4  // LM35 센서의 출력 핀이 연결된 ESP32-S3의 핀 번호

void setup() {
  Serial.begin(115200);           // 시리얼 통신 초기화
  analogReadResolution(12);       // 12비트 ADC 해상도 설정 (0~4095)
  Serial.println("LM35 온도 센서 사용 예제");
}

void loop() {
  int adcValue = analogRead(LM35_PIN);    // LM35 센서에서 아날로그 값 읽기
  float voltage = (adcValue / 4095.0) * 3.3;  // ADC 값을 전압으로 변환 (ESP32-S3의 참조 전압: 3.3V)
  float temperature = voltage * 100.0;       // 전압을 온도로 변환 (1V = 100°C)

  Serial.print("ADC 값: ");
  Serial.print(adcValue);
  Serial.print(" | 전압: ");
  Serial.print(voltage, 2);
  Serial.print(" V | 온도: ");
  Serial.print(temperature, 2);
  Serial.println(" °C");

  delay(1000);  // 1초 대기
}
```

## 1.9 RGB Led 센서 (15,21,16 번핀 red,green,blue)

이 프로그램은 RGB LED의 각 핀에 대해 LED의 밝기를 제어합니다. 빨강, 초록, 파랑, 흰색의 조합을 통해 다양한 색상을 순차적으로 출력합니다.

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="RGB Led 센서" width="100">  RGB Led 센서
```
15,21,16 이 차례로 red, green, blue 가 연결되어 있습니다. led 프로그램 해줘
```
아두이노 프로그램
```
// Define the RGB LED pins
const int redPin = 15;
const int greenPin = 21;
const int bluePin = 16;

void setup() {
  // Initialize the RGB LED pins as output
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
}

void loop() {
  // Red
  setColor(255, 0, 0); // Turn the RGB LED red
  delay(1000);         // Wait for a second
  // Green
  setColor(0, 255, 0); // Turn the RGB LED green
  delay(1000);         // Wait for a second
  // Blue
  setColor(0, 0, 255); // Turn the RGB LED blue
  delay(1000);         // Wait for a second
  // White
  setColor(255, 255, 255); // Turn the RGB LED white
  delay(1000);             // Wait for a second
  // Off
  setColor(0, 0, 0); // Turn the RGB LED off
  delay(1000);       // Wait for a second
}


// Function to set the color of the RGB LED
void setColor(int redValue, int greenValue, int blueValue) {
  analogWrite(redPin, redValue);
  analogWrite(greenPin, greenValue);
  analogWrite(bluePin, blueValue);
}
```

# Otto Ninja 로봇
배선연결 요약
|이름 | 핀번호 | 모터이름 |
|-----|-------|-------|
| LF | 7번 | servoLF |
| LL | 6번 | servoLL |
| RF | 5번 | servoRF |
| RL | 4번 | servoRL |

```
서보모터를 esp32 보드 i2r-05 에 연결합니다. LF 7번, LL 6번, RF 5번, RL 4번 핀에 연결 했습니다.
LF RF 는 180도 각도조절 서보모터이고 LL RL 은 360도 회전하는 서보모터 입니다.
ESP32Servo.h 를 이용하여 ninja otto 로봇을 아두이노 프로그램 하려고 합니다.
LF 7번 핀을 이용해서 회전 제어하는 예제 프로그램 만들어 주세요
```

✅ LF 서보모터 각도 테스트 프로그램 (핀 7번)
```
#include <ESP32Servo.h>

// LF 모터: 7번 핀, 이름: servoLF
const int LF_PIN = 7;
Servo servoLF;

void setup() {
  Serial.begin(115200);

  // 180도 서보모터 초기화
  servoLF.setPeriodHertz(50);  // 서보 주파수 설정 (일반적으로 50Hz)
  servoLF.attach(LF_PIN, 500, 2400);  // 최소/최대 펄스 폭 (마이크로초 단위)
  Serial.println("LF 서보모터 제어 시작");
}

void loop() {
  Serial.println("0도");
  servoLF.write(0);  // 0도 위치로 이동
  delay(1000);

  Serial.println("90도");
  servoLF.write(90);  // 90도 위치로 이동
  delay(1000);

  Serial.println("180도");
  servoLF.write(180);  // 180도 위치로 이동
  delay(1000);

  Serial.println("90도로 복귀");
  servoLF.write(90);  // 다시 중간 위치로
  delay(1000);
}
```

✅ LL 360 서보모터 전진 후진 테스트 프로그램 (핀 6번)
```
#include <ESP32Servo.h>

// LL 모터: 6번 핀, 이름: servoLL
Servo servoLL;

void setup() {
  Serial.begin(115200);
  servoLL.setPeriodHertz(50);
  servoLL.attach(6, 500, 2400);  // 핀 6번에 연결

  Serial.println("360도 서보모터 정지값 보정 테스트");
}

void loop() {
  // 전진
  servoLL.write(120);
  Serial.println("▶ 전진");
  delay(2000);

  // 정지 - 보정된 마이크로초 사용
  servoLL.writeMicroseconds(1500); // ← 필요시 1485~1515로 조정
  Serial.println("⏹ 정지");
  delay(2000);

  // 후진
  servoLL.write(60);
  Serial.println("◀ 후진");
  delay(2000);

  // 정지
  servoLL.writeMicroseconds(1500); // ← 다시 정지
  Serial.println("⏹ 정지");
  delay(2000);
}
```

✅ LL 360 서보모터 속도 조절 원리

|펄스(ms)	| 마이크로초(us) |	동작 |	속도 |
|---------|---------------|-----|--------|
|1.5ms	   | 1500          | 정지|  	0%   |
|   ↑     |	1600~2400	    | 전진|	느림 → 빠름|
|   ↓     |	1400~500      |	후진|	느림 → 빠름|


LL 서보모터 전진 속도제어 테스트 프로그램 (핀 6번)
속도제어는 1600 에서 2400까지 가능하나 저속에서 소리가만나고 회전하지 않을 때는 공급되는 전류가 약해서 그러니 건전지를 새것으로 교체하거나 별도의 외부 전원을 공급하면 정상 동작 합니다.
```
#include <ESP32Servo.h>

Servo servoLL;

void setup() {
  Serial.begin(115200);

  servoLL.setPeriodHertz(50);         // 서보모터용 50Hz 주파수
  servoLL.attach(6, 500, 2400);       // GPIO 6번, 500~2400us 펄스폭 설정

  Serial.println("LL 모터 전진 속도 증가 테스트 시작");
}

void loop() {
  // 1500us가 정지. 1520~1700까지 점점 빨라짐
  for (int pulse = 1700; pulse <= 1900; pulse += 10) {
    servoLL.writeMicroseconds(pulse);
    Serial.print("전진 PWM: ");
    Serial.print(pulse);
    Serial.println("us");
    delay(1000);  // 속도 변화 관찰을 위한 대기
  }

  // 정지
  servoLL.writeMicroseconds(1500);
  Serial.println("정지 (1500us)");
  delay(3000); // 다음 루프 전 잠시 대기
}
```

✅ 로봇 조립
Otto Ninja 로봇의 정확한 동작을 위해 왼쪽 다리(LL) 및 오른쪽 다리(RL)의 서보 모터는 반드시 90도(중립 위치)로 설정한 상태에서 조립해 주세요.    
이 위치에서 조립하지 않으면 걷기 동작이 비정상적으로 작동하거나 다리가 틀어질 수 있습니다.    

📌 TIP:
서보 모터에 전원을 공급한 후, 초기 위치(90도)로 이동시킨 다음 조립하세요.    
조립 전에 아래의 코드로 모터를 90도로 고정 한 후 조립하세요.    

```
#include <ESP32Servo.h>

// LF 서보모터를 7번 핀에 연결
const int LF_PIN = 7;
Servo servoLF;

// RF 서보모터를 5번 핀에 연결
const int RF_PIN = 5;
Servo servoRF;

void setup() {
  Serial.begin(115200);

  // 180도 서보모터 초기화
  servoLF.setPeriodHertz(50);
  servoLF.attach(LF_PIN, 500, 2400);

  servoRF.setPeriodHertz(50);
  servoRF.attach(RF_PIN, 500, 2400);

  Serial.println("LF RF 서보모터 제어 시작");

  Serial.println("servoLF 0도");
  servoLF.write(0);
  delay(1000);

  Serial.println("servoLF 90도");
  servoLF.write(90);
  delay(1000);

  Serial.println("servoLF 180도");
  servoLF.write(180);
  delay(1000);

  Serial.println("servoLF 90도");
  servoLF.write(90);
  delay(1000);

  Serial.println("servoRF 0도");
  servoRF.write(0);
  delay(1000);

  Serial.println("servoRF 90도");
  servoRF.write(90);
  delay(1000);

  Serial.println("servoRF 180도");
  servoRF.write(180);
  delay(1000);

  Serial.println("servoRF 90도");
  servoRF.write(90);
  delay(1000);
}

void loop() {
}
```

💻 로봇 전후진 프로그램
String command = "FORWARD";  // "FORWARD", "BACKWARD", "STOP"
command 설정에 따라 전진 후진 정지 하는 프로그램 입니다.
```
#include <ESP32Servo.h>
#include <Arduino.h>

// === 핀 번호 정의 ===
const int LF_PIN = 7;  // 180도 서보
const int RF_PIN = 5;  // 180도 서보
const int LL_PIN = 6;  // 360도 서보
const int RL_PIN = 4;  // 360도 서보

// === 서보 객체 정의 ===
Servo servoLF;
Servo servoRF;
Servo servoLL;
Servo servoRL;

// === 제어 명령 ===
String command = "FORWARD";  // "FORWARD", "BACKWARD", "STOP"

// === 동작 함수 정의 ===
void moveForward() {
  servoLF.write(180);
  servoRF.write(0);
  delay(500);
  servoLL.write(120);
  servoRL.write(120);
  Serial.println("▶ 전진");
}

void moveBackward() {
  servoLF.write(180);
  servoRF.write(0);
  delay(500);
  servoLL.write(60);
  servoRL.write(60);
  Serial.println("◀ 후진");
}

void stopMoving() {
  //servoLF.write(90);
  //servoRF.write(90);
  servoLL.writeMicroseconds(1500);
  servoRL.writeMicroseconds(1500);
  Serial.println("⏹ 정지");
}

void setup() {
  Serial.begin(115200);

  // 서보 초기화
  servoLF.setPeriodHertz(50);
  servoLF.attach(LF_PIN, 500, 2400);

  servoRF.setPeriodHertz(50);
  servoRF.attach(RF_PIN, 500, 2400);

  servoLL.setPeriodHertz(50);
  servoLL.attach(LL_PIN, 500, 2400);

  servoRL.setPeriodHertz(50);
  servoRL.attach(RL_PIN, 500, 2400);

  stopMoving();  // 초기 정지
  delay(3000);
  moveForward();
  delay(3000);
  stopMoving();
  moveBackward();
  delay(3000);
  stopMoving();
  
}

void loop() {
  // 명령 실행
  /*
  command.toUpperCase();
  if (command == "FORWARD") {
    moveForward();
  } else if (command == "BACKWARD") {
    moveBackward();
  } else {
    stopMoving();
  }
  */
}

```

✅ MQTT 통신에 의한 전진 후진 통신 프로그램
chatGpt 에 다음과 같이 요구하세 
```
아두이노 esp32 s3로 프로그램 합니다.
와이파이 연결은 ssid i2r password 00000000 입니다.
mqtt 서버는 ai.doowon.ac.kr 포트는 1883 
intopic i2r/kdi6033@gmail.com/in  outtopic i2r/kdi6033/out
프로토콜은 order=1 이면 전진, order=2 이면 후진하게 해줘
ArduinoJson.h를 사용해서 프로그램 해줘
전후진 프로그램은 앞의 예제를 참조해서 작성해줘
```
#### ✅ LL 모터만 전후진 아두이노 프로그램
출력된 아두이노 프로그램
mqtt 통신으로 {"order":1} 을 보내면 전진 {"order":2} 를 보내면 추진 합니다.
이것은 react로 작성하세요. 와이파이 정보와 intopic, outtopic은 자신의 것으로 수정하세요
```
#include <WiFi.h>
#include <PubSubClient.h>
#include <ArduinoJson.h>
#include <ESP32Servo.h>

// WiFi 정보
const char* ssid = "i2r";
const char* password = "00000000";

// MQTT 서버 정보
const char* mqtt_server = "ai.doowon.ac.kr";
const int mqtt_port = 1883;
const char* intopic = "i2r/kdi6033@gmail.com/in";
const char* outtopic = "i2r/kdi6033@gmail.com/out";

// 서보모터 관련
Servo servoLL;
const int servoPin = 6; // LL 모터 핀

WiFiClient espClient;
PubSubClient client(espClient);

// 서보 제어 함수
void controlServo(int order) {
  if (order == 1) {
    // 전진
    servoLL.writeMicroseconds(1800);
    Serial.println("전진 명령 - PWM: 1800us");
  } else if (order == 2) {
    // 후진
    servoLL.writeMicroseconds(1200);
    Serial.println("후진 명령 - PWM: 1200us");
  } else {
    // 정지
    servoLL.writeMicroseconds(1500);
    Serial.println("정지 명령 - PWM: 1500us");
  }
}

// MQTT 메시지 수신 콜백
void callback(char* topic, byte* payload, unsigned int length) {
  String msg;
  for (int i = 0; i < length; i++) {
    msg += (char)payload[i];
  }

  Serial.print("수신 메시지: ");
  Serial.println(msg);

  // JSON 파싱
  StaticJsonDocument<200> doc;
  DeserializationError error = deserializeJson(doc, msg);
  if (error) {
    Serial.print("JSON 파싱 실패: ");
    Serial.println(error.c_str());
    return;
  }

  int order = doc["order"];
  Serial.print("수신된 order: ");
  Serial.println(order);
  controlServo(order);
}

// MQTT 연결 함수
void reconnect() {
  while (!client.connected()) {
    Serial.print("MQTT 연결 시도 중...");
    String clientId = "ESP32Client-" + String(random(0xffff), HEX);
    if (client.connect(clientId.c_str())) {
      Serial.println("MQTT 연결 성공");
      client.subscribe(intopic);
    } else {
      Serial.print("실패, 상태코드: ");
      Serial.println(client.state());
      delay(2000);
    }
  }
}

void setup() {
  Serial.begin(115200);

  // 서보 초기화
  servoLL.setPeriodHertz(50);  // 서보 주파수 설정
  servoLL.attach(servoPin, 500, 2400); // 0도~180도에 해당하는 펄스 폭
  servoLL.writeMicroseconds(1500);  // 초기 상태 정지

  // WiFi 연결
  WiFi.begin(ssid, password);
  Serial.print("WiFi 연결 중");
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println("\nWiFi 연결 완료");

  // MQTT 설정
  client.setServer(mqtt_server, mqtt_port);
  client.setCallback(callback);
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();
}

```

#### ✅ LL RL 모터 전후진 아두이노 프로그램
chatGPT에 다음과 같이 요구한다.
```
https://github.com/kdi6033/i2r-05/blob/main/README.md#otto-ninja-%EB%A1%9C%EB%B4%87
여기 참조해서 LL(6번핀) RL(4번핀) 두개의 모터가 같이 동작해서 전진 후진 동작하게, 그리고 order=0 는 정지 하게  다음 프로그램 수정해줘
여기에 앞에 프로그램응 복사해서 넣어 주세요
```
```
#include <WiFi.h>
#include <PubSubClient.h>
#include <ArduinoJson.h>
#include <ESP32Servo.h>

// WiFi 정보
const char* ssid = "i2r";
const char* password = "00000000";

// MQTT 서버 정보
const char* mqtt_server = "ai.doowon.ac.kr";
const int mqtt_port = 1883;
const char* intopic = "i2r/kdi6033@gmail.com/in";
const char* outtopic = "i2r/kdi6033@gmail.com/out";

// 서보모터 관련
Servo servoLL;
const int servoPin = 6; // LL 모터 핀

WiFiClient espClient;
PubSubClient client(espClient);

// 서보 제어 함수
void controlServo(int order) {
  if (order == 1) {
    // 전진
    servoLL.writeMicroseconds(1800);
    Serial.println("전진 명령 - PWM: 1800us");
  } else if (order == 2) {
    // 후진
    servoLL.writeMicroseconds(1200);
    Serial.println("후진 명령 - PWM: 1200us");
  } else {
    // 정지
    servoLL.writeMicroseconds(1500);
    Serial.println("정지 명령 - PWM: 1500us");
  }
}

// MQTT 메시지 수신 콜백
void callback(char* topic, byte* payload, unsigned int length) {
  String msg;
  for (int i = 0; i < length; i++) {
    msg += (char)payload[i];
  }

  Serial.print("수신 메시지: ");
  Serial.println(msg);

  // JSON 파싱
  StaticJsonDocument<200> doc;
  DeserializationError error = deserializeJson(doc, msg);
  if (error) {
    Serial.print("JSON 파싱 실패: ");
    Serial.println(error.c_str());
    return;
  }

  int order = doc["order"];
  Serial.print("수신된 order: ");
  Serial.println(order);
  controlServo(order);
}

// MQTT 연결 함수
void reconnect() {
  while (!client.connected()) {
    Serial.print("MQTT 연결 시도 중...");
    String clientId = "ESP32Client-" + String(random(0xffff), HEX);
    if (client.connect(clientId.c_str())) {
      Serial.println("MQTT 연결 성공");
      client.subscribe(intopic);
    } else {
      Serial.print("실패, 상태코드: ");
      Serial.println(client.state());
      delay(2000);
    }
  }
}

void setup() {
  Serial.begin(115200);

  // 서보 초기화
  servoLL.setPeriodHertz(50);  // 서보 주파수 설정
  servoLL.attach(servoPin, 500, 2400); // 0도~180도에 해당하는 펄스 폭
  servoLL.writeMicroseconds(1500);  // 초기 상태 정지

  // WiFi 연결
  WiFi.begin(ssid, password);
  Serial.print("WiFi 연결 중");
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println("\nWiFi 연결 완료");

  // MQTT 설정
  client.setServer(mqtt_server, mqtt_port);
  client.setCallback(callback);
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();
}
```

## ✅ 1.3" OLED LCD 128x64
- Resolution: 128*64
- Control chip: SSH1106
- Display area: 29.42 x 14.7mm
- Driving voltage: 3.3-5V
- Operating temperature: -40 ℃ to 70 ℃
- Interface type: IIC/I2C  interface
- SSH1106은 SSD1306 컨트롤러와 호환됩니다. 차이점은 SSH1106은 RAM 공간이 132x64이지만 SSD1306은 128x64입니다. 그렇기 때문에 SSD1306프로그램 사용시 두번째 줄(0x02) 부터 화면을 시작하여 주셔야 합니다.
프로그램은 다음 두가지 라이브러리를 사용합니다. chatGPT 에서는  U8GLIB Library 를 추천 해서 이것으로 프로그램 합니다.
- U8GLIB Library
u8glib의 예제를 테스트하여 보시려면 아두이노 예제 스케치 코드 중 아래의 define문 comment처리를 제거한 후 컴파일하셔야 합니다.
U8GLIB_SSD1306_128X64 u8g(U8G_I2C_OPT_NONE); // I2C / TWI
- Adafruit_SSD1306 library
본 라이브러리를 사용하기 위해서는 Adafruit_GFX 라이브러리를 추가로 설치하셔야 합니다.
라이브러리의 예제코드를 테스트하기 위해서는 ssd1306_128x64_i2c.ino를 컴파일하셔야 합니다.
본 제품의 기본 I2C주소는 0x3C로 예제코드의 초기화 코드를 아래와 같이 변경하여야 합니다.
display.begin(SSD1306_SWITCHCAPVCC, 0x3C); // initialize with the I2C addr 0x3C (for the 128x64)

✅ "hello world" 츨력 프로그램
```
#include <Wire.h>
#include <U8g2lib.h>

// SH1106용 I2C 설정, FULL 버퍼
U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, /* reset=*/ U8X8_PIN_NONE);

void setup() {
  Wire.begin(18, 17);  // SDA=18, SCL=17
  u8g2.begin();
}

void loop() {
  u8g2.clearBuffer();
  u8g2.setFont(u8g2_font_ncenB14_tr); // 폰트 설정
  u8g2.drawStr(0, 32, "Hello World");
  u8g2.sendBuffer();
  delay(1000);
}
```

✅ "안녕하세요" 한글 츨력 프로그램
```
#include <Wire.h>
#include <U8g2lib.h>

// SH1106 I2C 디스플레이 설정 (SDA=18, SCL=17)
U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, U8X8_PIN_NONE);

void setup() {
  Wire.begin(18, 17);  // 사용자 설정 SDA, SCL
  u8g2.begin();
}

void loop() {
  u8g2.clearBuffer();

  // 유니폰트 한글 폰트 설정
  u8g2.setFont(u8g2_font_unifont_t_korean1);

  // 한글 유니코드로 출력
  u8g2.drawUTF8(0, 30, "안녕하세요!");

  u8g2.sendBuffer();
  delay(2000);
}
```

##### ✅ 눈동자 움직이는 그래픽 프로그램
```
#include <Wire.h>
#include <U8g2lib.h>

// SH1106 또는 SSD1306 OLED, I2C 연결
U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, U8X8_PIN_NONE);

int pupilX = 0;
int pupilY = 0;
int directionX = 1;
int directionY = 1;

void setup() {
  Wire.begin(18, 17);   // 사용자 SDA, SCL 설정
  u8g2.begin();
}

void loop() {
  // 눈 위치
  int eye1X = 32;
  int eye2X = 96;
  int eyeY = 32;
  int radius = 16;

  // 눈동자 위치 이동
  pupilX += directionX;
  pupilY += directionY;

  if (abs(pupilX) > 5) directionX = -directionX;
  if (abs(pupilY) > 3) directionY = -directionY;

  u8g2.clearBuffer();

  // 왼쪽 눈
  u8g2.drawCircle(eye1X, eyeY, radius, U8G2_DRAW_ALL);
  u8g2.drawDisc(eye1X + pupilX, eyeY + pupilY, 5, U8G2_DRAW_ALL);

  // 오른쪽 눈
  u8g2.drawCircle(eye2X, eyeY, radius, U8G2_DRAW_ALL);
  u8g2.drawDisc(eye2X + pupilX, eyeY + pupilY, 5, U8G2_DRAW_ALL);

  u8g2.sendBuffer();
  delay(100);
}
```
✅ 잠자는 눈동자 그래픽 프로그램
```
#include <Wire.h>
#include <U8g2lib.h>
#include <math.h>

U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, /* reset=*/ U8X8_PIN_NONE);

void setup() {
  Wire.begin(18, 17);      // 사용자 정의 I2C 핀: SDA=18, SCL=17
  u8g2.begin();
}

void loop() {
  u8g2.clearBuffer();

  drawSleepingEye(40, 32);  // 왼쪽 눈
  drawSleepingEye(88, 32);  // 오른쪽 눈

  u8g2.sendBuffer();
  delay(1000);
}

void drawSleepingEye(int cx, int cy) {
  const int radius = 16;
  const int eyelash_len = 5;
  const int start_deg = 30;
  const int end_deg = 150;

  // 눈꺼풀: 아래로 휘어진 부드러운 원호
  for (int angle = start_deg; angle <= end_deg; angle++) {
    float rad = angle * PI / 180.0;
    int x = cx + radius * cos(rad);
    int y = cy + radius * sin(rad);
    u8g2.drawPixel(x, y);
  }

  // 속눈썹: 원호 위에 일정 각도 간격으로, 접선의 수직 방향(법선 방향)으로 짧게 그리기
  for (int angle = start_deg; angle <= end_deg; angle += 10) {
    float rad = angle * PI / 180.0;

    int x1 = cx + radius * cos(rad);
    int y1 = cy + radius * sin(rad);

    // 접선의 수직 방향 = 원호의 법선 방향 (아래 방향)
    float dx = cos(rad + PI / 2.0);
    float dy = sin(rad + PI / 2.0);

    int x2 = x1 + eyelash_len * dx;
    int y2 = y1 + eyelash_len * dy;

    u8g2.drawLine(x1, y1, x2, y2);
  }
}
```

🟦 FastLED 라이브러리 사용하는 그래픽 프로그램

```
#include <FastLED.h>

#define NUM_LEDS 16
#define DATA_PIN 9
#define LED_TYPE WS2812B
#define COLOR_ORDER GRB

CRGB leds[NUM_LEDS];

void setup() {
  FastLED.addLeds<LED_TYPE, DATA_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.clear();
  FastLED.show();
}

void loop() {
  fill_solid(leds, NUM_LEDS, CRGB::Red);
  FastLED.show();
  delay(1000);

  fill_solid(leds, NUM_LEDS, CRGB::Green);
  FastLED.show();
  delay(1000);

  fill_solid(leds, NUM_LEDS, CRGB::Blue);
  FastLED.show();
  delay(1000);
}
```
🎨 색상표
| 색상명    | 코드                               |
| ------ | -------------------------------- |
| 빨강     | `CRGB::Red` or `CRGB(255,0,0)`   |
| 초록     | `CRGB::Green` or `CRGB(0,255,0)` |
| 파랑     | `CRGB::Blue` or `CRGB(0,0,255)`  |
| 노랑     | `CRGB::Yellow`                   |
| 시안(청록) | `CRGB::Cyan`                     |
| 보라     | `CRGB::Purple`                   |
| 흰색     | `CRGB::White`                    |
| 검정(꺼짐) | `CRGB::Black`                    |

##### ✅ 무지개 🌈 / 점멸 ✨ / 흐름 💨
```
#include <FastLED.h>

#define NUM_LEDS 16       // LED 개수
#define DATA_PIN 9        // 데이터 핀 (D9)
#define LED_TYPE WS2812B  // LED 종류
#define COLOR_ORDER GRB   // 색 순서

CRGB leds[NUM_LEDS];
uint8_t gHue = 0;         // 무지개 색상 변화용

void setup() {
  FastLED.addLeds<LED_TYPE, DATA_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.clear();
  FastLED.show();
}

void loop() {
  rainbowEffect();      // 무지개 효과
  blinkEffect();        // 점멸 효과
  flowingEffect();      // 흐름 효과
}

// 🌈 무지개 효과
void rainbowEffect() {
  for (int i = 0; i < 100; i++) {
    fill_rainbow(leds, NUM_LEDS, gHue++);
    FastLED.show();
    delay(50);
  }
}

// ✨ 점멸 효과
void blinkEffect() {
  for (int i = 0; i < 5; i++) {
    fill_solid(leds, NUM_LEDS, CRGB::White); // 켜짐
    FastLED.show();
    delay(300);

    fill_solid(leds, NUM_LEDS, CRGB::Black); // 꺼짐
    FastLED.show();
    delay(300);
  }
}

// 💨 흐름 효과 (앞에서 뒤로 번지는 느낌)
void flowingEffect() {
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB::Blue;
    if (i > 0) leds[i - 1] = CRGB::Black; // 이전 LED 끄기
    FastLED.show();
    delay(100);
  }
  leds[NUM_LEDS - 1] = CRGB::Black; // 마지막도 끄기
  FastLED.show();
}
```

| 효과  | 설명                               |
| --- | -------------------------------- |
| 무지개 | `fill_rainbow()` 함수로 자동 색상 변화 구현 |
| 점멸  | `fill_solid()`으로 흰색-검정 반복        |
| 흐름  | 하나의 LED가 켜지면서 앞에서 뒤로 이동하는 효과     |

🛠 응용 아이디어
흐름을 양방향으로 → i = NUM_LEDS-1 ~ 0 순회    
점멸 색상 랜덤화 → CHSV(random8(),255,255)    
무지개 속도 조절 → delay(10) 또는 EVERY_N_MILLISECONDS(20)    

## 🔰 VL53L0X Time-of-Flight (ToF) 거리 센서
<img src="https://github.com/user-attachments/assets/1e3b3bde-cb82-42ad-af43-7e03a7ce1e27" alt="VL53L0X" width="300">

### 🔍 개요
VL53L0X는 STMicroelectronics에서 개발한 **레이저 기반 Time-of-Flight(ToF) 거리 센서**입니다.  
적외선 레이저 펄스를 발사하고 반사되는 시간을 측정하여 **매우 정확한 거리**를 측정할 수 있습니다.  
광량, 반사율, 색상에 크게 영향을 받지 않아 안정적인 측정이 가능하며, 소형 폼팩터로 IoT, 로봇, HMI 등에 적합합니다.

---

### 📖 주요 사양

| 항목                  | 내용                                     |
|-----------------------|------------------------------------------|
| 센서 모델             | VL53L0X                                  |
| 측정 방식             | Time-of-Flight (ToF), 적외선 레이저 사용 |
| 측정 거리             | **30mm ~ 2000mm** (일반적으로 30cm 내외가 정확) |
| 정확도                | ±3% 이내                                 |
| 분해능                | 1mm 단위                                 |
| 동작 전압             | 2.6 ~ 3.5V (보통 3.3V 또는 5V 보드 전원 지원) |
| 인터페이스            | I2C (SCL, SDA)                           |
| 동작 온도             | -20°C ~ 70°C                             |
| 레이저 클래스         | Class 1 (안전함)                         |
| I2C 주소              | 기본: 0x29                               |
| 크기                  | 약 18mm x 12mm (보드에 따라 다름)         |

---

### ⚙️ 핀 설명 (보드에 따라 다름)

| 핀 이름 | 기능 설명                                      |
|---------|------------------------------------------------|
| VIN     | 전원 입력 (3.3V 또는 5V)                        |
| GND     | 접지                                           |
| SDA     | I2C 데이터                                     |
| SCL     | I2C 클럭                                       |
| XSHUT   | 전원 제어 (여러 센서 사용 시 주소 설정에 활용) |
| GPIO1   | 인터럽트 출력 (일반적으로 사용하지 않음)       |

---

### 🧩 응용 분야
- 로봇 거리 센서
- 장애물 회피
- 손 제스처 감지
- 사람 또는 물체 감지
- IoT 환경 거리 측정기


> 💻 예제 코드 
```
#include <Wire.h>
#include "Adafruit_VL53L0X.h"

Adafruit_VL53L0X lox = Adafruit_VL53L0X();

void setup() {
  Serial.begin(115200);
  delay(1000);

  // ESP32용 I2C 핀 설정 (SDA = 18, SCL = 17)
  Wire.begin(18, 17);

  // VL53L0X 초기화
  if (!lox.begin()) {
    Serial.println(F("VL53L0X 초기화 실패! 연결을 확인하세요."));
    while (1);
  }

  Serial.println(F("VL53L0X 거리 측정 시작"));
}

void loop() {
  VL53L0X_RangingMeasurementData_t measure;

  // 거리 측정 실행
  lox.rangingTest(&measure, false); // false: 디버그 출력 없음

  if (measure.RangeStatus != 4) {  // 4는 측정 실패
    Serial.print("거리: ");
    Serial.print(measure.RangeMilliMeter);
    Serial.println(" mm");
  } else {
    Serial.println("측정 실패");
  }

  delay(500);  // 0.5초 간격
}
```

##### 💻 통합 프로그램: OLED 눈 + LED 효과 + 거리 측정 출력 (Serial)
센서 3개를 통합해서 동작하는 프로그램
```
#include <FastLED.h>
#include <Wire.h>
#include <U8g2lib.h>
#include <math.h>
#include "Adafruit_VL53L0X.h"

// ------------------- OLED ---------------------
U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, /* reset=*/ U8X8_PIN_NONE);
int pupilX = 0, pupilY = 0;
int directionX = 1, directionY = 1;

// ------------------- FastLED ---------------------
#define NUM_LEDS 16
#define DATA_PIN 9
#define LED_TYPE WS2812B
#define COLOR_ORDER GRB
CRGB leds[NUM_LEDS];
uint8_t gHue = 0;
int mode = 1;  // 1:rainbow, 2:blink, 3:flow, 4:breath

// 타이머
unsigned long previousBlinkMillis = 0;
bool blinkState = false;
unsigned long previousFlowMillis = 0;
int flowIndex = 0;
unsigned long previousFrameMillis = 0;
const unsigned long frameInterval = 50;

// ------------------- Breathing ---------------------
int breathBrightness = 0;
bool breathUp = true;
unsigned long previousBreathMillis = 0;

// ------------------- VL53L0X ---------------------
Adafruit_VL53L0X lox = Adafruit_VL53L0X();
unsigned long previousDistanceMillis = 0;
const unsigned long distanceInterval = 500;

// ------------------- SETUP ---------------------
void setup() {
  Serial.begin(115200);
  delay(1000);

  Wire.begin(18, 17);  // I2C 핀 설정

  // VL53L0X 초기화
  if (!lox.begin()) {
    Serial.println(F("VL53L0X 초기화 실패!"));
    while (1);
  }

  u8g2.begin();

  FastLED.addLeds<LED_TYPE, DATA_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.clear();
  FastLED.show();

  Serial.println(F("시작 완료: OLED + LED + VL53L0X"));
}

// ------------------- LOOP ---------------------
void loop() {
  unsigned long currentMillis = millis();

  // 거리 측정 (0.5초 간격)
  if (currentMillis - previousDistanceMillis >= distanceInterval) {
    previousDistanceMillis = currentMillis;
    printDistance();
  }

  // 프레임 타이머
  if (currentMillis - previousFrameMillis >= frameInterval) {
    previousFrameMillis = currentMillis;

    updateEyeAnimation();

    switch (mode) {
      case 1: updateRainbowEffect(); break;
      case 2: updateBlinkEffect(); break;
      case 3: updateFlowingEffect(); break;
      case 4: updateBreathingEffect(); break;
    }
  }
}

// ------------------- VL53L0X ---------------------
void printDistance() {
  VL53L0X_RangingMeasurementData_t measure;
  lox.rangingTest(&measure, false);

  if (measure.RangeStatus != 4) {
    Serial.print("거리: ");
    Serial.print(measure.RangeMilliMeter);
    Serial.println(" mm");
  } else {
    Serial.println("측정 실패");
  }
}

// ------------------- Eye ---------------------
void updateEyeAnimation() {
  int eye1X = 32, eye2X = 96, eyeY = 32, radius = 16;

  pupilX += directionX;
  pupilY += directionY;
  if (abs(pupilX) > 5) directionX = -directionX;
  if (abs(pupilY) > 3) directionY = -directionY;

  u8g2.clearBuffer();
  u8g2.drawCircle(eye1X, eyeY, radius, U8G2_DRAW_ALL);
  u8g2.drawDisc(eye1X + pupilX, eyeY + pupilY, 5, U8G2_DRAW_ALL);
  u8g2.drawCircle(eye2X, eyeY, radius, U8G2_DRAW_ALL);
  u8g2.drawDisc(eye2X + pupilX, eyeY + pupilY, 5, U8G2_DRAW_ALL);
  u8g2.sendBuffer();
}

// ------------------- FastLED Effects ---------------------
void updateRainbowEffect() {
  fill_rainbow(leds, NUM_LEDS, gHue++);
  FastLED.show();
}

void updateBlinkEffect() {
  unsigned long currentMillis = millis();
  if (currentMillis - previousBlinkMillis >= 300) {
    previousBlinkMillis = currentMillis;
    blinkState = !blinkState;
    fill_solid(leds, NUM_LEDS, blinkState ? CRGB::White : CRGB::Black);
    FastLED.show();
  }
}

void updateFlowingEffect() {
  unsigned long currentMillis = millis();
  if (currentMillis - previousFlowMillis >= 100) {
    previousFlowMillis = currentMillis;

    fill_solid(leds, NUM_LEDS, CRGB::Black);
    leds[flowIndex] = CRGB::Blue;
    flowIndex = (flowIndex + 1) % NUM_LEDS;

    FastLED.show();
  }
}

void updateBreathingEffect() {
  unsigned long currentMillis = millis();
  if (currentMillis - previousBreathMillis >= 20) {
    previousBreathMillis = currentMillis;

    if (breathUp) {
      breathBrightness += 5;
      if (breathBrightness >= 255) {
        breathBrightness = 255;
        breathUp = false;
      }
    } else {
      breathBrightness -= 5;
      if (breathBrightness <= 0) {
        breathBrightness = 0;
        breathUp = true;
      }
    }

    fill_solid(leds, NUM_LEDS, CHSV(gHue, 255, breathBrightness));
    FastLED.show();
  }
}
```
