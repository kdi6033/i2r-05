<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=220&section=header&text=Arduino%20Board%20i2r-05&fontSize=50&animation=fadeIn&fontAlignY=38&desc=IoT%20%C2%B7%20%ED%94%BC%EC%A7%80%EC%BB%AC%20AI%20%C2%B7%20%EC%98%A8%EB%94%94%EB%B0%94%EC%9D%B4%EC%8A%A4%20AI%20%EA%B8%B0%EB%B0%98%EC%9D%98%20%EC%8A%A4%EB%A7%88%ED%8A%B8%20%EA%B3%B5%EC%9E%A5%20%EC%9E%90%EB%8F%99%ED%99%94%20%EC%86%94%EB%A3%A8%EC%85%98&descAlignY=55&descAlign=50" />
</div>

<div align="center">
  <a href="https://i2r.link">🌐 공식 홈페이지</a> &nbsp;&nbsp; | &nbsp;&nbsp;
  <a href="https://i2r.link/products">🛒 i2r 제품구매</a> &nbsp;&nbsp; | &nbsp;&nbsp;
  <a href="https://www.youtube.com/@i2r-link">▶️ YouTube</a>
</div>

---
## ✅ 1. i2r-05 AI IoT 아두이노 보드 (KC 전파인증)

🎯 개요   

i2r-05 보드를 활용하여 기본적인 하드웨어 이해부터 실습을 진행하고, Physical AI On-Device AI(온디바이스 AI) 구현합니다. 그리고 스마트팜을 하시는 분들을 위해서 각종 센서와 액튜에이터를 자동으로 연결하여 스마트폰과 PC에서 모니터링/제어 할 수 있게 합니다.

🎯 교육 목표    

- i2r-05 보드를 활용하여 하드웨어 및 펌웨어 개발의 기초를 익힘
- Wi-Fi 및 MQTT 기반의 IoT 통신을 실습하여 네트워크 프로그래밍 이해
- 머신러닝 및 On-Device AI 개념을 학습하고 실제 보드에서 실행 가능하도록 구현
- ESP32-S3의 강력한 연산 성능을 활용하여 실시간 데이터 분석 및 처리

## ✅ 2. 🤖 AI로 코드 자동 생성

**코딩 경험 없어도 됩니다!**

1. [claude.ai](https://claude.ai) 접속
2. 채팅창에 아래 붙여넣기:
```
https://raw.githubusercontent.com/kdi6033/i2r-05/main/CLAUDE.md
읽고 [원하는 동작을 한국어로 설명]
```

**예시:**
- `DHT11로 습도 측정하고 40% 넘으면 부져 울려줘`
- `온도 30도 넘으면 부저 울려줘`
- `스위치 누르면 LED 켜줘`  
- `WiFi 연결하고 MQTT로 센서 데이터 보내줘`

→ 완성 코드 복사 → Arduino IDE 붙여넣기 → 업로드

## ✅ 3. i2r-05 보드 사양

📌 ESP32-S3-WROOM-1-N16R8 설명
ESP32-S3-WROOM-1-N16R8은 Espressif Systems에서 개발한 고성능 Wi-Fi 및 Bluetooth LE 모듈입니다. 이 모듈은 ESP32-S3 SoC를 기반으로 하며, **16MB의 플래시 메모리(N16)와 8MB의 PSRAM(R8)**을 탑재하고 있습니다.

ESP32 S3 16M Flash, AI IoT 개발용 보드

<img src="https://github.com/user-attachments/assets/4ba415d9-08e6-4b2c-9396-1d3f35ffdfe2?raw=true" height="300">    

<img src="https://github.com/user-attachments/assets/ed673ea3-f054-4370-ae92-979a29e72c4d?raw=true" height="300">    

📌 i2r-05 보드 핀맵

| 기능        | GPIO |  설명         |
| --------- | ---- | ---------- |
| TX\_USB   | IO43 | USB TX     |
| RX\_USB   | IO44 | USB RX     |
| SCL (I2C) | IO17 | I2C 클럭     |
| SDA (I2C) | IO18 | I2C 데이터    |
| USB\_DN   | IO19 | USB D-     |
| USB\_DP   | IO20 |  USB D+     |
| FR\_SW    | IO45 | 기능 스위치     |
| LED\_RGB  | IO48 | 내장 RGB LED |


✅ 1. 주요 특징    

🟢 (1) CPU 및 성능    
- 듀얼코어 Xtensa® LX7 32비트 프로세서
- 최대 240MHz 클럭 속도
- AI 및 DSP 기능 향상 (벡터 연산 가속 지원)
  
🟢 (2) 메모리    
- 16MB 플래시 메모리 (N16)
- 8MB PSRAM (R8) → AI, 이미지 처리, 데이터 버퍼링에 유용
  
🟢 (3)무선 기능     
- Wi-Fi 802.11 b/g/n (2.4GHz)
- Bluetooth 5.0 LE (Low Energy)
- WPA3 보안 지원
  
🟢 (4) USB 기능    
- Full-Speed USB OTG (USB 1.1)
- USB CDC/JTAG 디버깅 지원
- USB-Serial 통신 가능 (UART 필요 없음)
  
🟢 (5) GPIO 및 확장성    
- 최대 45개의 GPIO 핀 제공
- SPI, I2C, UART, PWM, ADC, DAC 지원
- JTAG 디버깅 지원
  
🟢 (6) 저전력 설계    
- Deep Sleep 모드에서 μA 단위의 전력 소모
- ULP (Ultra-Low Power) 코프로세서 내장
  
🟢 (7) AI 및 머신러닝    
- Vector Extension (AI 가속기) 포함
- TensorFlow Lite, ESP-DSP 최적화 지원


✅ 2. ESP32-S3-WROOM-1-N16R8의 장점    
- 대용량 PSRAM (8MB) 탑재 : 이미지 처리, AI 모델, 오디오 스트리밍 등에 적합
- Wi-Fi + Bluetooth 동시 지원 : BLE를 활용한 IoT 기기 및 스마트 디바이스 개발 가능
- USB OTG 지원 : 직접 USB 장치와 통신 가능 (키보드, 마우스, 스토리지 연결)
- 보안 기능 강화 : Secure Boot, Flash Encryption, AES-XTS 암호화 지원
- ESP-IDF 및 Arduino 지원 : ESP-IDF, Arduino, MicroPython 등 다양한 개발 환경 제공

✅ 3. ESP32-S3-WROOM-1-N16R8의 활용 사례    
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

✅ 4. ESP32-S3-WROOM-1-N16R8 개발 환경    
- ESP-IDF (Espressif 공식 SDK)
- Arduino IDE
- Visual Code
- PlatformIO
- MicroPython
- FreeRTOS 기반 멀티태스킹 지원

arduino IDE를 사용하여 컴파일 하려면 tool 에서 보드설정은 아래와 같습니다.    

<img width="250" src="https://github.com/user-attachments/assets/786d4d17-e62d-4c16-bae7-ef9bf459cffe" />    


<br>     
custom 으로 설정하면 partition.csv 를 참조합니다. 다음은 chatgpt 또는 gemini 에게 부탁해 작성한 파일입니다. 참조하세요
<details>
    <summary>💻 partitions.csv 16M Flash 설계</summary>

```c
# Name,   Type, SubType, Offset,   Size,       Flags
nvs,      data, nvs,     0x9000,   0x5000,
otadata,  data, ota,     0xe000,   0x2000,
app0,     app,  ota_0,   0x10000,  0x600000,
app1,     app,  ota_1,   0x610000, 0x600000,
coredump, data, coredump,0xC10000, 0x10000,
spiffs,   data, spiffs,  0xC20000, 0x3D0000,
```
</details>

-----

📌 보드의 RGB Led 제어 (48번핀)
보드에는 RGB Led가 48번으로 장착되었습니다. 다음은 색상을 제어하는 프로그램 입니다.    

🔗 [▶️ 유튜브 보기 - ** ChatGPT AI IoT 아두이노 보드  RGB Led 제어 (48번핀)**](https://youtu.be/dB-iA1lIVrQ)

 [▶️ 유튜브 보기 - **Antigravity AI IoT 아두이노 보드  RGB Led 제어 (48번핀)**](https://youtu.be/Z3YIdUVMx4M)

> 보드에는 RGB Led가 48번으로 장착되었습니다.  이 Led의 색상을 제어하는 프로그램 입니다.
> 무지게, 점멸,흐름 효과 프로그램

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  💻 48번 RGB Led 제어    
```
esp32 s3 를 사용하고 48번핀에 RGB Led  가 연결되 있습니다. 이 한선으로 칼라를 제어 합니다. 빨강 파랑 녹색 불들어오게 프로그램 해줘
```

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
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
</details>


Adafruit_NeoPixel 는 내부에 인터럽트를 사용하여 I2c와 충돌이 일어 나서 제어용 프로그램과 함깨 구성하면 에러가 자주 발생하여 FastLED.h 를 사용해서 Led를 제어 합니다.   
이는 I2C와 충돌이 일어 날 수 있으나 앞에 프로그램 보다는 효율적 입니다.    
다음은 무지개 효과, 점멸, 밝기를 조절하는 프로그램 입니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100"> 💻 무지게, 점멸,흐름 효과 프로그램    
```
esp32 s3 를 사용하고 48번핀에 RGB Led  가 연결되 있습니다. FastLED.h를 이용해서 무지게, 점멸,흐름 효과 프로그램 해줘
```

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
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
</details>

-----------

## ✅ 4. 아두이노로 구현하는 Physical AI 챗봇 (feat. ESP32 & Gemini)

> 단순히 모니터 속에 갇힌 챗봇이 아닙니다. 카메라/센서로 사람을 인식하고, 마이크로 명령을 이해하며, 스스로 말하고 기계(릴레이 등)를 조작하는 진짜 **'물리적 인공지능(Physical AI)'**을 아두이노(ESP32-S3)로 구현하는 프로젝트입니다.

<img width="600" alt="i2r Shield V1" src="https://github.com/kdi6033/i2r-05/raw/main/images/ai_chatbot_pipeline.png?raw=true" />     

**💡 요약 (3줄 핵심 원리)**

> step1: **내 음성을 구글 도움으로 문자로 만들고** (음성 인식 / STT)    
> step2: **그 문자로 구글 AI에게 문자로 답변 받고** (대화형 AI / LLM)    
> step3: **그 답변 문자를 구글 도움으로 음성으로 출력** (음성 합성 / TTS)

----

**🟢 Step 1: 내 음성을 구글 도움으로 문자로 만들고 (음성 인식 / STT)**

**① 음성 녹음 (마이크 ➡️ 보드)**
* 사용자가 말하면 보드의 마이크(INMP441)가 음성을 녹음하여 비압축 오디오(WAV) 형태로 임시 저장합니다.
  * *기술 상세:* 마이크의 소리 크기를 실시간으로 감지하여 말이 시작되면 자동으로 녹음하고, 조용해지면 녹음을 마칩니다. (단, 0.12초 이하의 짧은 충격음 노이즈는 자동으로 필터링합니다.)

**② 음성 인식 (보드 ➡️ 구글 Gemini ➡️ 질문 텍스트)**
* 보드가 이 WAV 데이터(Base64 인코딩)를 구글(Gemini API)로 보내면, AI가 음성을 알아듣고 **사용자의 질문 텍스트**로 변환하여 돌려줍니다.


**🟢 Step 2: 그 문자로 구글 AI에게 문자로 답변 받고 (대화형 AI / LLM)**

**③ 답변 생성 (질문 텍스트 ➡️ 구글 Gemini ➡️ 답변 텍스트)**
* 변환된 질문 텍스트를 다시 구글 AI(Gemini API)에 보내면, AI가 상황에 맞게 생각하여 **AI의 답변 텍스트**를 생성해 돌려줍니다.
  * *기술 상세:* 이때 단순한 텍스트뿐만 아니라 **과거 대화 기록(최대 10턴)**을 함께 덧붙여서 전송하기 때문에 이전 대화의 문맥을 기억하며 자연스럽게 대답할 수 있습니다.


**🟢 Step 3: 그 답변 문자를 구글 도움으로 음성으로 출력 (음성 합성 / TTS)**

**④ 음성 출력 (답변 텍스트 ➡️ 구글 TTS ➡️ 스피커)**
* 최종 답변 텍스트를 구글 번역기(TTS)로 보내 **MP3 오디오 스트리밍 데이터**를 실시간으로 받아오고, 보드가 이를 스피커(MAX98357A)로 출력해 줍니다.
  * *기술 상세:* 끊김 없이 매끄러운 대화를 위해 응답 지연을 방지하는 스마트 타임아웃이 적용되어 있습니다. 음성 출력이 완전히 끝남을 감지하면(스트림 종료 후 2초 경과), 곧바로 **Step 1** 상태로 복귀하여 사용자의 다음 질문을 자동으로 듣기 시작합니다.

---

📌  목차

1. [사용 부품](#-사용-부품)
2. [핀 연결 - 스피커 (MAX98357A)](#-핀-연결---스피커-max98357a)
3. [핀 연결 - 마이크 (INMP441)](#-핀-연결---마이크-inmp441)
4. [전체 연결 다이어그램](#-전체-연결-다이어그램)
5. [동작 원리](#-동작-원리)
6. [단어 입력 → 음성 출력 상세 과정](#-단어-입력--음성-출력-상세-과정)
7. [개발 환경 설정](#-개발-환경-설정)
8. [코드 설명](#-코드-설명)
9. [주요 기술 개념](#-주요-기술-개념)
10. [문제 해결](#-문제-해결)

---

📌  사용 부품

| 부품 | 모델명 | 설명 |
|------|--------|------|
| **메인 보드** | i2r-05보드 | ESP32-S3-WROOM-1-N16R8, 16MB Flash + 8MB PSRAM, WiFi 내장 |
| **오디오 앰프** | MAX98357A | I2S 디지털 입력 → 스피커 출력 앰프 |
| **스피커** | 4Ω 또는 8Ω, 3W 이상 | 소리를 출력하는 스피커 |
| **마이크** | INMP441 | I2S MEMS 디지털 마이크 |

> **N16R8 모델명 해석**  
> - **N16** = Flash 메모리 16MB (프로그램 저장소)  
> - **R8**  = PSRAM 8MB (실행 중 사용하는 RAM)

---

📌  핀 연결 - 스피커 (MAX98357A)

**I2S 신호선 (MAX98357A ↔ i2r-05 보드)**

| MAX98357A 핀 | i2r-05 핀 | 신호 이름 | 역할 |
|-------------|----------|----------|------|
| **DIN** | **GPIO 11** | Data In | 오디오 데이터 전송 |
| **BCLK** | **GPIO 12** | Bit Clock | 데이터 동기화 클럭 |
| **LRCLK** | **GPIO 13** | LR Clock | 좌/우 채널 구분 |
| **SD** | **GPIO 14** | Shutdown | HIGH = 앰프 ON, LOW = 음소거 |

📌 전원 및 공통선

| MAX98357A 핀 | i2r-05 핀 | 역할 |
|-------------|----------|------|
| **VCC** | **3.3V** | 전원 공급 |
| **GND** | **GND** | 공통 접지 |
| **GAIN** | **GND** | 이득 설정 (GND = 0dB, VCC = 6dB) |

📌 스피커 연결

| 스피커 선 | MAX98357A 단자 | 설명 |
|---------|--------------|------|
| **🔴 빨간색 (양극)** | **OUT+** | 스피커 + 극 |
| **⚫ 검은색 (음극)** | **OUT-** | 스피커 - 극 |

---

📌 핀 연결 - 마이크 (INMP441)

**I2S 신호선 (INMP441 ↔ i2r-05 보드)**

| INMP441 핀 | i2r-05 핀 | 역할 |
|-----------|----------|------|
| **VDD** | **3.3V** | 전원 (⚠️ 반드시 3.3V! 5V 연결 시 파손) |
| **GND** | **GND** | 접지 |
| **L/R** | **GND** | 채널 선택 (GND = 왼쪽 채널 사용) |
| **SCK** | **GPIO 9** | I2S 비트 클럭 |
| **WS** | **GPIO 10** | I2S 채널 클럭 (Word Select) |
| **SD** | **GPIO 8** | I2S 데이터 출력 (마이크 → ESP32) |

> ⚠️ **L/R 핀을 반드시 GND에 연결**하세요!  
> 연결하지 않으면 마이크가 랜덤 채널을 선택하여 소리가 잡히지 않습니다.

> ⚠️ **스피커(MAX98357A) SD핀과 마이크(INMP441) SD핀은 다른 핀입니다!**  
> 스피커 SD = GPIO 14 (앰프 ON/OFF)  
> 마이크 SD = GPIO 8 (데이터 출력)

---

📌  전체 연결 다이어그램

📌 스피커 연결

```
i2r-05 보드 (ESP32-S3-N16R8)         MAX98357A 오디오 앰프
┌──────────────────────────┐           ┌──────────────────────┐
│                          │           │                      │
│  GPIO 11 (DIN)  ─────────┼───────────┤ DIN  (오디오 데이터) │
│  GPIO 12 (BCLK) ─────────┼───────────┤ BCLK (비트 클럭)     │
│  GPIO 13 (LRCLK)─────────┼───────────┤ LRCLK(채널 클럭)     │
│  GPIO 14 (SD)   ─────────┼───────────┤ SD   (앰프 ON/OFF)   │
│                          │           │                      │
│  3.3V    ────────────────┼───────────┤ VCC  (전원)          │
│  GND     ────────────────┼───────────┤ GND  (접지)          │
│                          │           │ GAIN ──── GND        │
└──────────────────────────┘           │                      │
                                       │  OUT+ ──── 🔴 스피커 │
                                       │  OUT- ──── ⚫ 스피커 │
                                       └──────────────────────┘
```

📌 마이크 연결

```
i2r-05 보드 (ESP32-S3-N16R8)         INMP441 마이크
┌──────────────────────────┐           ┌──────────────────────┐
│                          │           │                      │
│  GPIO  8 (SD)   ─────────┼───────────┤ SD   (마이크 데이터) │
│  GPIO  9 (SCK)  ─────────┼───────────┤ SCK  (비트 클럭)     │
│  GPIO 10 (WS)   ─────────┼───────────┤ WS   (채널 클럭)     │
│                          │           │                      │
│  3.3V    ────────────────┼───────────┤ VDD  (전원 3.3V!)    │
│  GND     ────────────────┼───────────┤ GND  (접지)          │
│  GND     ────────────────┼───────────┤ L/R  (채널 선택)     │
└──────────────────────────┘           └──────────────────────┘
```

📌 전체 핀 사용 요약

```
i2r-05 보드
┌─────────────────────────────────────────────┐
│  GPIO  8 ── INMP441 SD    (마이크 데이터)   │
│  GPIO  9 ── INMP441 SCK   (마이크 클럭)     │
│  GPIO 10 ── INMP441 WS    (마이크 채널)     │
│                                             │
│  GPIO 11 ── MAX98357A DIN  (스피커 데이터)  │
│  GPIO 12 ── MAX98357A BCLK (스피커 클럭)    │
│  GPIO 13 ── MAX98357A LRCLK(스피커 채널)    │
│  GPIO 14 ── MAX98357A SD   (앰프 ON/OFF)    │
│                                             │
│  3.3V ── INMP441 VDD, MAX98357A VCC         │
│  GND  ── INMP441 GND/L/R, MAX98357A GND     │
└─────────────────────────────────────────────┘
```

---

📌  동작 원리

```
[텍스트 입력]
     │
     ▼
[ESP32-S3]
  ① 텍스트를 URL 인코딩
     예) "안녕하세요" → "%EC%95%88%EB%85%95%ED%95%98%EC%84%B8%EC%9A%94"
     │
  ② WiFi로 Google TTS 서버에 HTTP 요청
     URL: http://translate.google.com/translate_tts?tl=ko&q=...
     │
  ③ MP3 오디오 스트림을 수신 (인터넷에서 음성 파일 다운로드)
     │
  ④ ESP32-audioI2S 라이브러리가 MP3를 실시간 디코딩
     │
  ⑤ I2S 프로토콜로 MAX98357A 앰프에 전송
     (GPIO 11=데이터, GPIO 12=클럭, GPIO 13=채널선택)
     │
  ⑥ MAX98357A가 디지털 신호 → 아날로그 증폭
     │
     ▼
[스피커에서 한국어 음성 출력] 🔊
```

---

📌  단어 입력 → 음성 출력 상세 과정

**Step 1: 텍스트 입력 수신**

시리얼 모니터에서 "안녕하세요" 입력 후 Enter를 누르면
`loop()` 함수가 이를 감지합니다.

```cpp
// loop() 안에서 실행
String input = Serial.readStringUntil('\n');
// input = "안녕하세요"
speakKorean(input);   // 다음 단계로 전달
```

**Step 2: 한글 → URL 인코딩 변환**

한글은 인터넷 URL에 바로 사용할 수 없습니다.
각 바이트를 `%XX` 형식으로 변환합니다.

```
"안녕하세요"  ←  UTF-8 바이트로 분해
  안 = EC 95 88  →  %EC%95%88
  녕 = EB 85 95  →  %EB%85%95
  하 = ED 95 98  →  %ED%95%98
  세 = EC 84 B8  →  %EC%84%B8
  요 = EC 9A 94  →  %EC%9A%94

결과: "%EC%95%88%EB%85%95%ED%95%98%EC%84%B8%EC%9A%94"
```

**Step 3: Google TTS 서버에 HTTP 요청**

URL을 완성하여 WiFi로 Google 서버에 접속합니다.

```
http://translate.google.com/translate_tts
  ?ie=UTF-8          ← 인코딩 방식
  &client=tw-ob      ← 클라이언트 식별자
  &tl=ko             ← 언어: 한국어(Korean)
  &q=%EC%95%88...    ← 인코딩된 텍스트
```

```
여러분의 ESP32-S3          인터넷           Google 서버
      │                                          │
      │──── HTTP 요청 (URL로 접속) ────────────→ │
      │                                          │ 텍스트를
      │                                          │ MP3로 변환
      │ ←──── MP3 파일 데이터 전송 ─────────── │
      │                                          │
    재생!
```

**Step 4: MP3 스트리밍 수신 + 디코딩**

> **"다운로드 후 재생"이 아닌 "받으면서 동시에 재생"입니다!**

```
Google 서버
  └─ MP3 데이터를 조금씩 전송 (스트리밍)
          ↓
ESP32-S3 PSRAM (8MB)
  └─ 수신된 MP3를 720KB 버퍼에 임시 저장
          ↓
ESP32-audioI2S 라이브러리
  └─ MP3 압축 해제 → PCM(날것의 오디오 샘플) 변환
     (16000Hz, 16bit 오디오 데이터)
```

| 방식 | 설명 | 이 프로젝트 |
|------|------|------------|
| **다운로드** | 파일 전체를 받은 후 재생 | ❌ 사용 안 함 |
| **스트리밍** | 받으면서 동시에 재생 | ✅ 사용 |

**Step 5: I2S로 앰프에 전송**

```
ESP32-S3 내부 I2S 하드웨어
  GPIO 12 (BCLK)  → 초당 수십만 번 클럭 신호
  GPIO 13 (LRCLK) → 좌/우 채널 구분 신호
  GPIO 11 (DIN)   → 오디오 데이터 비트 전송
          ↓
MAX98357A 칩이 수신
```

**Step 6: 디지털 → 아날로그 변환 + 증폭**

```
MAX98357A 내부:
  ① DAC : 디지털 비트 → 아날로그 전압 파형으로 변환
  ② 앰프 : 미세한 신호 → 스피커를 구동할 수 있는 전력으로 증폭
           (최대 3.7W @ 4Ω)
          ↓
OUT+ / OUT- 단자 → 스피커 코일에 전류 흘림
  → 진동판 떨림 → 공기 진동 → 귀에 소리로 인식! 🔊
```

**⏱ 전체 타임라인**

```
0ms      Enter 누름
  │
10ms     loop()에서 텍스트 읽기 완료
  │
20ms     URL 인코딩 완료
  │
50ms     WiFi TCP 연결 (Google 서버)
  │
200ms    HTTP 응답 시작 (첫 MP3 데이터 수신)
  │
500ms    버퍼 충분히 채워짐 → 재생 시작! 🔊
  │
(재생 중) audio.loop()가 계속 호출되며 스트리밍 유지
  │
끝       audio_eof_mp3() 콜백 → "[Audio] 재생 완료" 출력
```

**❓ 자주 나오는 질문**

**Q: MP3 파일을 ESP32에 저장하나요?**
> **아니오!** 저장하지 않습니다. 받으면서 바로 재생(스트리밍)합니다.
> 재생이 끝나면 데이터는 버려집니다.

**Q: 매번 Google 서버에 접속하나요?**
> **네!** 텍스트를 입력할 때마다 매번 인터넷으로 요청합니다.
> 따라서 **WiFi가 없으면 소리가 나지 않습니다.**

**Q: 내가 입력한 텍스트가 Google에 전송되나요?**
> **네.** URL에 텍스트가 담겨 Google 서버로 전송됩니다.
> 나중에 보안이 중요하다면 **로컬 TTS** 또는 **유료 API** 사용을 권장합니다.

**Q: `audio.loop()`는 왜 loop()에 있어야 하나요?**
> 스트리밍 데이터를 계속 받아서 처리하기 위해서입니다.
> 이 줄이 없으면 첫 버퍼만 재생되고 음성이 중간에 멈춥니다.

**Q: API 키가 없어도 사용할 수 있나요?**
> **네, API 키 없이 사용 가능합니다!**
> 이 프로젝트의 URL은 Google Translate 웹사이트가 내부적으로 사용하는
> **비공식(undocumented) 무료 엔드포인트**입니다.

📌 비공식 vs 공식 Google TTS 비교

| 구분 | 이 프로젝트 (비공식) | Google Cloud TTS (공식) |
|------|---------------------|------------------------|
| **API 키** | ❌ 불필요 | ✅ 필요 |
| **비용** | 완전 무료 | 월 100만 자 무료, 이후 유료 |
| **텍스트 길이** | 약 200자 제한 | 최대 5,000자 |
| **안정성** | 구글이 언제든 차단 가능 ⚠️ | 안정적 보장 ✅ |
| **음질** | 보통 | 고품질 (WaveNet 등) |
| **상업적 사용** | ❌ 불가 | ✅ 가능 |
| **용도** | 학습, 프로토타입 | 실제 서비스, 제품 |

> ⚠️ **학생 실습 주의사항**
> - 비공식 API이므로 **교육 목적으로만** 사용하세요.
> - 간혹 Google이 요청을 차단하면 소리가 나지 않을 수 있습니다.
> - LLM 챗봇 등 실제 서비스에 연결할 때는 **공식 TTS API** 사용을 권장합니다.

---

📌 개발 환경 설정

**1단계: Arduino IDE 설치**
- [Arduino IDE 다운로드](https://www.arduino.cc/en/software)

**2단계: ESP32 보드 패키지 설치**
Arduino IDE → **File → Preferences → Additional boards manager URLs** 에 추가:
```
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```
그 다음 **Tools → Board Manager → "esp32"** 검색 → 설치

**3단계: ESP32-audioI2S 라이브러리 설치**
**Tools → Manage Libraries → "ESP32-audioI2S" 검색 → Install**
- 제작자: **schreibfaul1**
- 버전: **3.4.5** 이상

**4단계: Arduino IDE 보드 설정**

**Tools** 메뉴에서 아래와 같이 설정:

| 항목 | 설정값 |
|------|--------|
| Board | **ESP32S3 Dev Module** |
| Flash Size | **16MB (128Mb)** |
| **PSRAM** | **OPI PSRAM** ← 반드시 설정! |
| Partition Scheme | **Custom** (또는 16M Flash) |
| Upload Speed | 921600 |

> ⚠️ **PSRAM 설정이 가장 중요합니다!**  
> 오디오 스트리밍에 720KB 버퍼가 필요한데, PSRAM을 활성화해야 사용 가능합니다.

**5단계: WiFi 설정 변경**
`speak.ino` 파일에서 본인 WiFi 정보로 수정:
```cpp
#define WIFI_SSID      "본인_WiFi_이름"
#define WIFI_PASSWORD  "본인_WiFi_비밀번호"
```

---

📌  코드 설명

**전체 구조 (`speak.ino`)**

```
speak.ino
├── urlEncode()      한글 → URL 인코딩 변환
├── speakKorean()    Google TTS로 음성 재생
├── connectWiFi()    WiFi 연결
├── checkPsram()     PSRAM 메모리 확인
├── setup()          초기화 (1회 실행)
│   ├── PSRAM 확인
│   ├── 앰프 활성화 (SD 핀 HIGH)
│   ├── WiFi 연결
│   ├── I2S 오디오 초기화
│   └── 부팅 시 음성 테스트
├── loop()           반복 실행
│   ├── audio.loop()  ← 스트리밍 유지 (필수!)
│   └── 시리얼 입력 수신 → speakKorean() 호출
└── 콜백 함수들
    ├── audio_info()       오디오 상태 출력
    ├── audio_eof_mp3()    재생 완료 알림
    └── audio_showstation() 스테이션 정보 출력
```

📌 핵심 코드 해설

**① URL 인코딩 (`urlEncode`)**
한국어(UTF-8)는 인터넷 URL에 바로 사용할 수 없습니다.  
각 바이트를 `%XX` 형식으로 변환합니다.

```cpp
// "안" (UTF-8: EC 95 88) → "%EC%95%88"
String urlEncode(const String& text) {
    // 영문자/숫자는 그대로, 나머지는 %XX 형식으로 변환
    sprintf(hex, "%%%02X", c);  // c = 바이트 값
}
```

**② Google TTS 호출 (`speakKorean`)**
```cpp
String url = "http://translate.google.com/translate_tts"
             "?ie=UTF-8&client=tw-ob&tl=ko&q=" + encoded;
//                                     ^^^^^
//                                     tl=ko : 한국어 설정

audio.connecttohost(url.c_str());  // MP3 스트리밍 시작
```

**③ I2S 오디오 초기화 (`setup`)**
```cpp
audio.setPinout(PIN_I2S_BCLK,   // GPIO 12: 비트 클럭
                PIN_I2S_LRC,    // GPIO 13: 채널 클럭
                PIN_I2S_DOUT);  // GPIO 11: 데이터

audio.setVolume(18);  // 볼륨: 0(무음) ~ 21(최대)
```

**④ 앰프 활성화**
```cpp
pinMode(PIN_I2S_SD, OUTPUT);    // GPIO 14를 출력으로 설정
digitalWrite(PIN_I2S_SD, HIGH); // HIGH → MAX98357A 앰프 ON
// LOW로 하면 음소거됩니다
```

**⑤ 스트리밍 유지 (`loop`)**
```cpp
void loop() {
    audio.loop();  // ← 이 줄이 없으면 소리가 끊깁니다!
                   //   반복적으로 호출해야 MP3 스트리밍 지속
}
```

---

📌 주요 기술 개념

**I2S (Inter-IC Sound) 프로토콜**
디지털 오디오를 칩 간에 전송하는 표준 프로토콜입니다.

```
ESP32-S3                MAX98357A
  GPIO 12 (BCLK)  ──→  각 비트의 타이밍을 알려주는 신호
  GPIO 13 (LRCLK) ──→  Left/Right 채널을 구분하는 신호
  GPIO 11 (DIN)   ──→  실제 오디오 데이터 (0과 1)
```

**TTS (Text-to-Speech)**
텍스트를 음성으로 변환하는 기술입니다.  
이 프로젝트에서는 **Google Translate의 무료 TTS API**를 사용합니다.

```
내 코드 → Google 서버 → MP3 음성 파일 → 스피커
```

> 💡 인터넷 연결이 필요합니다. WiFi가 없으면 소리가 나지 않습니다.

**PSRAM (Pseudo Static RAM)**
ESP32-S3 칩 내부 RAM은 512KB로 제한됩니다.  
오디오 스트리밍 버퍼(720KB)를 담기에 부족하므로,  
외부에 붙어있는 PSRAM 8MB를 사용합니다.

```
내부 SRAM  512 KB  ← 코드 실행용
PSRAM     8 MB   ← 오디오 버퍼용 (Arduino IDE에서 활성화 필요!)
Flash     16 MB  ← 프로그램 저장소
```

**MP3 스트리밍**
전체 파일을 다운로드하지 않고, 받으면서 동시에 재생합니다.  
`ESP32-audioI2S` 라이브러리가 이를 자동으로 처리합니다.

```
Google 서버 → [조금씩 수신] → [실시간 MP3 디코딩] → I2S → 스피커
              ↑ 버퍼링 필요 (PSRAM에 임시 저장)
```

---

📌  문제 해결

**문제 1: `OOM: failed to allocate 720896 bytes`**
**원인**: PSRAM이 비활성화되어 있음  
**해결**: Arduino IDE → **Tools → PSRAM → OPI PSRAM**

**문제 2: `'class Audio' has no member named 'setBufsize'`**
**원인**: ESP32-audioI2S v3.x에서 해당 함수가 제거됨  
**해결**: `setBufsize()` 호출 코드를 삭제

**문제 3: WiFi는 연결되는데 소리가 안 남**
**원인 및 확인 순서**:
1. 시리얼 모니터에서 `[PSRAM] 감지됨` 메시지 확인
2. `[Audio]` 메시지가 출력되는지 확인
3. SD 핀(GPIO 14) 연결 확인 (HIGH = 앰프 ON)
4. 스피커 연결 방향 확인 (빨강=OUT+, 검정=OUT-)
5. 볼륨 설정 확인 (`audio.setVolume(18)`)

**문제 4: Google TTS URL 오류**
**원인**: Google TTS는 비공식 API로 간헐적으로 차단될 수 있음  
**해결**: 잠시 기다리거나, 유료 TTS API(OpenAI, ElevenLabs 등)로 교체

📌 시리얼 모니터 정상 출력 예시
```
=================================
  ESP32-S3 한국어 TTS 스피커
=================================
[PSRAM] 감지됨! 크기: 8388608 bytes (8.0 MB)
[RAM] 여유 힙: 327680 bytes (320 KB)
[OK] 앰프 활성화 (SD=HIGH)
[WiFi] 연결 시도: i2r
..
[WiFi] 연결됨! IP: 192.168.0.36
[OK] PSRAM 사용 → 고품질 스트리밍
[OK] I2S 오디오 초기화 완료
────────────────────────────────
[TTS] 텍스트: 안녕하세요! 스피커 테스트입니다.
[TTS] URL: http://translate.google.com/...
[Audio] 재생 완료
```

---

📌 다음 단계: LLM 연결

이 프로젝트의 `speakKorean()` 함수를 활용하면 LLM(대형 언어 모델)의 응답을 바로 음성으로 출력할 수 있습니다:

```cpp
// LLM에서 받은 응답 텍스트를 음성으로 출력
String llmResponse = "오늘 날씨는 맑고 기온은 25도입니다.";
speakKorean(llmResponse);  // 바로 음성 출력!
```

📌 전체 AI 챗봇 구조 (목표)
```
[마이크] → [음성 인식(STT)] → [LLM 서버] → [TTS(speak.ino)] → [스피커]
INMP441       Whisper API       OpenAI/etc    Google TTS        MAX98357A
```

---

📌 ESP32-S3 한국어 음성인식(STT) 프로젝트

> **INMP441 마이크**로 음성을 녹음하고 **Gemini 2.5 Flash API**로 한국어 텍스트를 인식하는 프로젝트입니다.  
> 파일: `mike/mike.ino`

---

📌  STT 프로젝트 목차

1. [동작 흐름 한눈에 보기](#-동작-흐름-한눈에-보기)
2. [Gemini API 키 발급 방법](#-gemini-api-키-발급-방법)
3. [Google Cloud 설정](#-google-cloud-설정)
4. [코드에 API 키 입력](#-코드에-api-키-입력)
5. [실행 과정 상세 설명](#-실행-과정-상세-설명)
6. [시리얼 모니터 출력 해석](#-시리얼-모니터-출력-해석)
7. [STT 기술 원리](#-stt-기술-원리)
8. [문제 해결 (STT)](#-문제-해결-stt)

---

**🔄 동작 흐름 한눈에 보기**

```
[학생이 Enter 누름]
        ↓
[INMP441 마이크로 2초 녹음]
  → I2S 디지털 신호로 수신
  → PCM 16kHz, 16bit 오디오 데이터
        ↓
[WAV 파일 만들기]
  → 44바이트 WAV 헤더 + PCM 데이터
  → PSRAM에 저장 (약 62KB)
        ↓
[Base64 인코딩]
  → 바이너리 → 텍스트 변환
  → HTTPS 전송을 위한 변환 (약 83KB)
        ↓
[Gemini 2.5 Flash API 전송]
  → HTTPS POST 요청
  → generativelanguage.googleapis.com
        ↓
[Gemini AI가 음성 분석]
  → "이 오디오의 한국어 내용을 텍스트로만 출력해줘"
        ↓
[시리얼 모니터에 결과 출력]
  → [인식 결과] 안녕하세요
```

---

📌  Gemini API 키 발급 방법

**1단계: Google AI Studio 접속**

```
https://aistudio.google.com
```

- Google 계정으로 로그인

**2단계: API 키 발급**

```
왼쪽 사이드바 하단 → "Get API key" 클릭
        ↓
"새 API 키 만들기" 클릭
        ↓
키 이름: i2r-chatbot (원하는 이름)
프로젝트: 새 프로젝트 만들기
        ↓
"키 만들기" 클릭
        ↓
AIzaSy... 로 시작하는 키 복사!
```

> ⚠️ **API 키는 절대 다른 사람과 공유하지 마세요!**

**3단계: 무료 사용 한도**

| 항목 | 무료 한도 |
|------|---------|
| 하루 요청 수 | **1,500회** |
| 분당 요청 수 | **15회** |
| 토큰 (분당) | 1,000,000 토큰 |

> 교육용으로 충분한 양입니다!

---

📌  Google Cloud 설정

**왜 Google Cloud 설정이 필요한가?**

Gemini API는 Google Cloud 프로젝트와 연결되어 있습니다.  
**무료로 사용해도** 결제 계정 연결이 필요합니다.

**1단계: 결제 계정 연결**

```
https://console.cloud.google.com/billing
        ↓
"계정 만들기" 클릭
        ↓
카드 정보 입력 (무료 한도 내 요금 없음)
        ↓
"프로젝트" 탭 → i2r-chatbot 프로젝트 찾기
        ↓
결제 계정 연결
```

**2단계: Gemini API 활성화 확인**

```
https://console.cloud.google.com/apis/library/generativelanguage.googleapis.com
        ↓
"Gemini API" 페이지 열림
        ↓
"● API 사용 설정됨" 확인 (이미 활성화됨)
```

**3단계: API 키 제한 설정 확인**

```
https://console.cloud.google.com/apis/credentials
        ↓
API 키 클릭
        ↓
"애플리케이션 제한사항" → "없음" 확인
"API 제한사항" → "제한 없음" 확인
```

---

📌  코드에 API 키 입력

`mike/mike.ino` 파일 38번째 줄:

```cpp
// ── Gemini API 키 ──────────────────────────────────────────
#define GEMINI_API_KEY "여기에_발급받은_키_입력"
// 예시:
#define GEMINI_API_KEY "AIzaSyAbcdef1234567890XXXXXXXXXX"
```

> 반드시 큰따옴표 `" "` 안에 키를 넣어야 합니다!

📌 WiFi 설정도 변경

```cpp
#define WIFI_SSID      "내_WiFi_이름"    // 예: "i2r"
#define WIFI_PASSWORD  "내_WiFi_비밀번호" // 예: "00000000"
```

---

📌 실행 과정 상세 설명

**① 부팅 및 초기화**

```
[시리얼 모니터 출력]

==============================
  음성인식 데모 (Gemini STT)  
==============================
[PSRAM] WAV: 62KB, Base64: 83KB 할당 완료
[OK] 마이크 초기화 완료
[WiFi] i2r 연결 중...
[WiFi] 연결됨! IP: 192.168.0.36
```

| 출력 | 의미 |
|------|------|
| `WAV: 62KB` | 2초 녹음 버퍼 (16kHz × 2초 × 2바이트) |
| `Base64: 83KB` | WAV를 텍스트로 변환한 크기 |
| `마이크 초기화 완료` | I2S 마이크 정상 연결 확인 |
| `IP: 192.168.0.36` | WiFi 연결 성공 |

**② 녹음**

```
[녹음] 🔴 말씀하세요! (2초)
[녹음] ⬛ 완료!
[Base64] 인코딩 완료: 83 KB
```

| 출력 | 의미 |
|------|------|
| `🔴 말씀하세요!` | 지금 말하면 됩니다! |
| `⬛ 완료!` | 2초 녹음 완료 |
| `인코딩 완료: 83KB` | API 전송 준비 완료 |

**③ API 전송 및 결과**

```
[STT] Gemini API 전송 중...
[DEBUG] 응답길이: 1057

──────────────────────────────
[인식 결과] 안녕하세요
──────────────────────────────
```

| 출력 | 의미 |
|------|------|
| `응답길이: 1057` | Gemini 서버가 보낸 응답 크기 |
| `[인식 결과] 안녕하세요` | ✅ 인식 성공! |

---

📌 시리얼 모니터 출력 해석

**정상 동작**

```
[녹음] 🔴 말씀하세요! (2초)   ← 지금 말하세요!
[녹음] ⬛ 완료!
[Base64] 인코딩 완료: 83 KB
[STT] Gemini API 전송 중...
[DEBUG] 응답길이: 1057         ← 숫자가 크면 정상
[인식 결과] 안녕하세요          ← 성공!
```

**오류 출력 해석**

| 출력 | 원인 | 해결 |
|------|------|------|
| `[오류] Gemini 서버 연결 실패` | WiFi 연결 안됨 | SSID/비밀번호 확인 |
| `[인식 실패]` + 응답길이 0 | API 키 오류 | API 키 재확인 |
| `429 quota exceeded` | 분당 요청 초과 | 1분 기다렸다 재시도 |
| `404 not found` | 모델명 오류 | 코드의 모델명 확인 |
| `[인식 실패]` + 응답길이 1000+ | 파싱 오류 | 코드 업데이트 필요 |

---

📌  STT 기술 원리

**I2S 마이크 (INMP441)**

```
소리 (아날로그)
    ↓
INMP441 내부 ADC 변환
    ↓
I2S 디지털 신호 (0과 1)
    ↓ SCK(클럭), WS(채널), SD(데이터)
ESP32-S3 수신
```

**WAV 파일 구조**

```
[44바이트 WAV 헤더]     ← 파일 형식 정보
  RIFF, WAVE, fmt
  샘플레이트: 16000Hz
  비트심도: 16bit
  채널: 1(모노)
[PCM 데이터 64000바이트] ← 실제 소리 데이터
  = 16000Hz × 2초 × 2바이트
```

**Base64 인코딩**

```
바이너리 데이터: 11110000 10110011 ...
        ↓
텍스트 변환: "8LM..." (A-Z, a-z, 0-9, +, / 만 사용)
        ↓
HTTPS JSON에 포함 가능해짐
```

> 바이너리 3바이트 → 텍스트 4글자로 변환되어 크기가 약 33% 증가합니다.

**Gemini API 요청 구조**

```json
{
  "contents": [{
    "parts": [
      {
        "inline_data": {
          "mime_type": "audio/wav",
          "data": "Base64로_인코딩된_WAV_데이터"
        }
      },
      {
        "text": "이 오디오의 한국어 내용을 텍스트로만 출력해줘"
      }
    ]
  }]
}
```

**Gemini API 응답 구조**

```json
{
  "candidates": [{
    "content": {
      "parts": [{
        "text": "안녕하세요"
      }]
    }
  }]
}
```

---

**🔧 문제 해결 (STT)**

**PSRAM 오류**

```
[오류] PSRAM 없음! Tools → PSRAM → OPI PSRAM
```

**해결:**
```
Arduino IDE → Tools → PSRAM → "OPI PSRAM" 선택
```

📌  WiFi 연결 실패

```
[WiFi] i2r 연결 중...
...............
```

**해결:**
```cpp
// SSID와 비밀번호 확인
#define WIFI_SSID      "정확한_WiFi_이름"
#define WIFI_PASSWORD  "정확한_비밀번호"
```

**인식률이 낮을 때**

| 원인 | 해결 |
|------|------|
| 마이크 거리 너무 멀음 | 마이크에서 5~10cm 거리에서 말하기 |
| 주변 소음 | 조용한 환경에서 테스트 |
| 말하는 속도가 빠름 | 천천히 또렷하게 발음 |
| L/R 핀 미연결 | INMP441의 L/R 핀 → GND 연결 확인 |

**분당 요청 초과 (429 오류)**

```
여러 번 연속 테스트하면 429 오류 발생
→ 1분 기다린 후 재시도
```

---

📌  다음 단계: TTS + STT 통합 챗봇

현재 구현된 두 프로그램을 연결하면:

```
[마이크로 질문]
INMP441 → mike.ino → Gemini STT
        ↓
[AI가 답변 생성]
Gemini API (텍스트 응답)
        ↓
[스피커로 답변 출력]
speak.ino → Google TTS → MAX98357A → 스피커
```

```cpp
// 통합 예시 코드 구조
void loop() {
  String question = listenAndTranscribe();  // STT
  String answer   = askGemini(question);    // AI 답변
  speakKorean(answer);                      // TTS
}
```

---

📌  참고 자료

| 항목 | 링크 |
|------|------|
| ESP32-audioI2S 라이브러리 | https://github.com/schreibfaul1/ESP32-audioI2S |
| MAX98357A 데이터시트 | https://datasheets.maximintegrated.com/en/ds/MAX98357A.pdf |
| ESP32-S3 기술 문서 | https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/ |
| i2r-05 보드 GitHub | https://github.com/kdi6033/i2r-05 |
| Arduino ESP32 설치 | https://docs.espressif.com/projects/arduino-esp32/en/latest/ |
| Google AI Studio | https://aistudio.google.com |
| Gemini API 문서 | https://ai.google.dev/gemini-api/docs |
| Gemini 요금 안내 | https://ai.google.dev/gemini-api/docs/rate-limits |


-----------

## ✅ 5. 3.5" IPS LCD HMI

i2r-05 보드로 3.5" IPS LCD를 제어하는 방법을 설명합니다.

---

📌 1. 부품 목록

| 부품 | 사양 |
|------|------|
| MCU | i2r-06 (ESP32-S3 기반) |
| LCD | 3.5인치 IPS SPI LCD (320×480) |
| 디스플레이 IC | ILI9488 |
| 터치 IC | XPT2046 (저항막 방식) |
| PLC | i2r-02 (ESP32 기반, 4채널 입출력) |

---

📌 2. LCD 핀 연결 

상업용 PCB 설계 시 ESP32-S3의 **8~16번 핀(연속된 9개 핀)**을 활용하여 가장 효율적이고 안정적으로 설계하는 핀맵입니다.

| i2r-06 (ESP32-S3) | LCD 핀 번호 | LCD 핀 이름 | 역할 및 배선 가이드 (PCB 설계 시 주의점) |
|:------:|:-----------:|:-----------:|:------|
| **5V** | 1 | VDD | **반드시 5V** (3.3V 시 터치 오작동) |
| GND | 2 | GND | 공통 접지 |
| **GPIO 8** | 3 | CS | LCD Chip Select |
| **GPIO 9** | 4 | RST | LCD 리셋 |
| **GPIO 10** | 5 | DC | 데이터/커맨드 선택 |
| **GPIO 11** | 6 & 12 | SDI & TDI | **MOSI 공유**: PCB에서 LCD 6번과 12번을 묶어서 ESP 11번에 연결 |
| **GPIO 12** | 7 & 10 | SCK & TCK | **SCK 공유**: PCB에서 LCD 7번과 10번을 묶어서 ESP 12번에 연결 |
| **GPIO 13** | 8 | BL | 백라이트 제어 |
| ❌ **연결 금지** | **9** | **SDO** | **절대 연결 금지 (N.C)**: ILI9488 하드웨어 버그로 버스 충돌 유발 |
| **GPIO 14** | 11 | TCS | 터치 Chip Select |
| **GPIO 15** | 13 | TDO | **MISO**: 터치 데이터 출력 |
| **GPIO 16** | 14 | PEN (IRQ) | 터치 인터럽트 |

----
TFT_eSPI 라이브러리를 설치하고 \Arduino\libraries\TFT_eSPI\
이 폴더 안에 있는 기존 User_Setup.h를 프로젝트의 User_Setup.h로 덮어쓰기:
TFT_eSPI 라이브러리에 "내 LCD 드라이버와 연결 핀이 이것"이라고 알려주는 필수 설정 파일입니다.


<br>     
<details>
    <summary>💻 User_Setup.h </summary>

```c
// TFT_eSPI User_Setup - AliExpress 3.5" IPS ILI9488 (i2r-06 ESP32-S3)
// 핀 연결 가이드: lcd_github.md 참조

#define USER_SETUP_INFO "IPS-ILI9488 3.5 i2r-06-ESP32S3"

// ----- Section 1: Driver -----
#define ILI9488_DRIVER

// 3.5" 320x480 (portrait)
#define TFT_WIDTH  320
#define TFT_HEIGHT 480

// IPS 패널 색 반전
#define TFT_INVERSION_ON

// ----- Section 2: Pins (Commercial PCB Layout) -----
#define TFT_CS    8    // LCD CS (LCD 3번)
#define TFT_RST   9    // LCD Reset (LCD 4번)
#define TFT_DC    10   // LCD Data/Command (LCD 5번)
#define TFT_MOSI  11   // LCD SDI + 터치 TDI 공유 (LCD 6, 12번)
#define TFT_SCLK  12   // LCD SCK + 터치 TCK 공유 (LCD 7, 10번)
#define TFT_BL    13   // 백라이트 (LCD 8번)
#define TFT_MISO  15   // 터치 TDO (LCD 13번)
#define TFT_BACKLIGHT_ON HIGH

// 터치 (XPT2046)
#define TOUCH_CS  14   // 터치 CS (LCD 11번)
#define TOUCH_IRQ  16   // 터치 IRQ (LCD 14번)

// ----- Section 3: ESP32-S3 SPI -----
// ESP32-S3에서 Octal Flash/PSRAM 사용 시 SPI2(FSPI)가 시스템에 예약되므로,
// 충돌을 피하기 위해 반드시 SPI3(HSPI)를 사용하도록 강제 지정합니다.
#define USE_HSPI_PORT

// ----- Section 4: SPI speed -----
#define SPI_FREQUENCY       20000000
#define SPI_READ_FREQUENCY  16000000
#define SPI_TOUCH_FREQUENCY  2500000

// ----- Section 5: Fonts -----
#define LOAD_GLCD   // Font 1
#define LOAD_FONT2  // Font 2
#define LOAD_FONT4  // Font 4
#define LOAD_FONT6  // Font 6
#define LOAD_FONT7  // Font 7
#define LOAD_FONT8  // Font 8
#define LOAD_GFXFF  // FreeFonts
#define SMOOTH_FONT
```
</details>



<br>     
<details>
    <summary>💻 예제1: 2초마다 배경색을 빨강→초록→파랑으로 순환하며 화면 중앙에 "Hello world"를 흰색으로 표시합니다. </summary>

```c
// i2r-06 (ESP32-S3) + 3.5" IPS ILI9488 LCD "Hello world" 테스트
// 핀: SCK=15, MOSI=16, MISO=12, CS=10, DC=21, RST=9, BL=14
// 터치: TCS=13, TIRQ=11

#include <TFT_eSPI.h>

TFT_eSPI tft = TFT_eSPI();

void setup() {
  Serial.begin(115200);

  // 백라이트 켜기
  pinMode(TFT_BL, OUTPUT);
  digitalWrite(TFT_BL, TFT_BACKLIGHT_ON);

  // TFT 초기화
  tft.init();
  tft.setRotation(1); // 가로 모드
  tft.fillScreen(TFT_BLACK);

  // 텍스트 설정 (흰색, 배경 투명)
  tft.setTextColor(TFT_WHITE);
  
  // 화면 정중앙에 "Hello world" 출력 (폰트 크기 4)
  tft.drawCentreString("Hello world", 240, 160, 4);

  Serial.println("Hello world Displayed!");
}

int color_state = 0;

void loop() {
  delay(2000); // 2초 대기
  
  // 색상 변경 테스트
  if (color_state == 0) {
    tft.fillScreen(TFT_RED);
    color_state = 1;
  } else if (color_state == 1) {
    tft.fillScreen(TFT_GREEN);
    color_state = 2;
  } else {
    tft.fillScreen(TFT_BLUE);
    color_state = 0;
  }
  
  // 배경이 바뀔 때마다 글자를 다시 그려줍니다
  tft.setTextColor(TFT_WHITE);
  tft.drawCentreString("Hello world", 240, 160, 4);
}

```
</details>



<br>     
<details>
    <summary>💻 에제2: 터치 버튼을 누를 때마다 버튼 색이 빨강(OFF)↔초록(ON)으로 토글되는 터치 UI 예제입니다. </summary>

```c
// i2r-06 (ESP32-S3) + 3.5" IPS LCD 상업용 핀맵 예제
// 핀: SCK=12, MOSI=11, MISO=15, CS=8, DC=10, RST=9, BL=13
// 터치: TCS=14, TIRQ=16

#include <TFT_eSPI.h>

TFT_eSPI tft = TFT_eSPI();

bool buttonState = false;
bool lastTouchState = false;

// 버튼 UI 영역 (화면 중앙, 480x320 기준)
const int btnX = 140;
const int btnY = 110;
const int btnW = 200;
const int btnH = 100;

void drawButton() {
  uint16_t btnColor = buttonState ? TFT_GREEN : TFT_RED;
  String btnText = buttonState ? "ON" : "OFF";
  
  // 버튼 배경 그리기
  tft.fillRoundRect(btnX, btnY, btnW, btnH, 15, btnColor);
  
  // 버튼 텍스트 그리기
  tft.setTextColor(TFT_WHITE);
  tft.drawCentreString(btnText, btnX + btnW / 2, btnY + btnH / 2 - 12, 4);
}

bool getTouchCoords(int16_t &x, int16_t &y) {
  uint16_t rx = 0, ry = 0;
  
  // TIRQ 핀이 LOW이면 터치된 상태
  if (digitalRead(TOUCH_IRQ) == LOW) {
    if (tft.getTouchRaw(&rx, &ry)) {
      // lcd_github.md 캘리브레이션 실측값 기반 좌표 매핑
      // rx: Y축 raw 값, ry: X축 raw 값
      x = map(ry, 204, 3781, 0, 480);
      y = map(rx, 3808, 311, 0, 320);
      
      // 화면 밖으로 나가는 값 잘라내기
      x = constrain(x, 0, 479);
      y = constrain(y, 0, 319);
      return true;
    }
  }
  return false;
}

void setup() {
  Serial.begin(115200);

  pinMode(TFT_BL, OUTPUT);
  digitalWrite(TFT_BL, TFT_BACKLIGHT_ON);
  pinMode(TOUCH_IRQ, INPUT_PULLUP); // 터치 인터럽트 핀 풀업

  tft.init();
  tft.setRotation(1); // 가로 모드 (480x320)
  tft.fillScreen(TFT_BLACK);

  // 상단 제목 출력
  tft.setTextColor(TFT_WHITE);
  tft.drawCentreString("Touch Button Test", 240, 40, 4);

  // 첫 버튼 그리기
  drawButton();
}

void loop() {
  int16_t x, y;
  bool isTouched = getTouchCoords(x, y);

  // 터치가 시작된 순간(Edge)만 감지
  if (isTouched && !lastTouchState) {
    Serial.printf("Touch Detected at (X: %d, Y: %d)\n", x, y);
    
    // 터치된 좌표가 버튼 영역 안인지 확인
    if (x >= btnX && x <= btnX + btnW && y >= btnY && y <= btnY + btnH) {
      buttonState = !buttonState; // 상태 반전 (ON/OFF)
      drawButton();               // 버튼 화면 갱신
      Serial.println(buttonState ? "Button Toggled: ON" : "Button Toggled: OFF");
    }
  }
  
  lastTouchState = isTouched;
  delay(20); // 터치 디바운싱
}

```
</details>





----

## ✅ 6. i2r-shield-01 보드

<img width="600" alt="i2r Shield V1" src="https://github.com/kdi6033/i2r-05/raw/main/images/i2r-shield-01-3.png?raw=true" />    

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
| 15 | RGB LED red D9 | 빨간색 Led 입력 핀 |
| 21 | RGB LED green D10 | 녹색 Led 입력 핀 |
| 16 | RGB LED blue D11 | 파란색 Led 입력 핀 |
| 12 | IR Receiver D6 | 	적외선 리모컨을 이용한 제어 가능 |
| 14 | D8           | 디지털핀 |
| 13 | D7           | 디지털핀 |
| 5 | A3           | 아나로그핀 |


------------------------------------------------------

## 📌 5.1 Led 제어 (47, 38 번핀)
ESP32-S3 보드의 47번 핀과 38번 핀에 연결된 LED를 1초 간격으로 교차로 점등하는 Arduino 프로그램입니다.    

🔗 [▶️ 유튜브 보기 - **AI IoT 아두이노 보드 와이파이 연결과 LED**](https://youtu.be/pZmccYi0Sho)

🔗 [▶️ 유튜브 보기 - **Antigravity 와 LED**](https://youtu.be/2vXIVVjECGM)

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100"> 💻  47, 38번 Led 제어    
```
esp32 s3 보드 47, 38번 핀에 led가 연결되어 있습니다. 1초 간격으로 교차로 점등하게 프록램 해줘요
```


<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
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
</details>

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100"> 💻 와이파이 연결과 Led    
```
와이파이 연결프로그램 만들어줘 ssid:i2r pw:00000000
처음에 빨간색 led, 연결되면 파란색 led 불들어오게 프로그램 해줘
led는 low 일 때 on 됩니다.
```

<br>     
<details>
    <summary>💻 아두이노 프로그램 </summary>

```c
#include <WiFi.h>

// Wi-Fi 설정
const char* ssid = "i2r";
const char* password = "00000000";

// LED 핀 설정 (LOW일 때 ON)
const int RED_LED_PIN = 47;
const int BLUE_LED_PIN = 38;

void setup() {
  Serial.begin(115200);

  // LED 핀을 출력으로 설정
  pinMode(RED_LED_PIN, OUTPUT);
  pinMode(BLUE_LED_PIN, OUTPUT);

  // 초기 상태: 빨간 LED ON, 파란 LED OFF
  digitalWrite(RED_LED_PIN, LOW);   // 빨간색 ON
  digitalWrite(BLUE_LED_PIN, HIGH); // 파란색 OFF

  // Wi-Fi 연결 시도
  WiFi.begin(ssid, password);
  Serial.print("Wi-Fi 연결 시도 중");

  int retry = 0;
  while (WiFi.status() != WL_CONNECTED && retry < 20) {
    delay(500);
    Serial.print(".");
    retry++;
  }

  if (WiFi.status() == WL_CONNECTED) {
    Serial.println("\n✅ Wi-Fi 연결 성공!");
    digitalWrite(RED_LED_PIN, HIGH);   // 빨간색 OFF
    digitalWrite(BLUE_LED_PIN, LOW);   // 파란색 ON
  } else {
    Serial.println("\n❌ Wi-Fi 연결 실패!");
    // 빨간 LED 유지
  }
}

void loop() {
  // 연결 상태 유지 확인용
}

```
</details>

-------------------------------------------------------------------------

## 📌 5.2 스위치 입력 (8, 9 번핀)
ESP32-S3 보드의 8번 핀과 9번 핀에 연결된 스위치를 감지하고, 스위치를 누를 때마다 시리얼 포트로 해당 상태를 출력하는 Arduino 프로그램입니다.  
🔗 [▶️ 유튜브 보기 - **AI IoT 아두이노 보드 스위치 입력**](https://youtu.be/KBWlxocToo8)    
🔗 [▶️ 유튜브 보기 - **Antigravity IoT 아두이노 보드 스위치 입력**](https://youtu.be/rGXK1YXbcC0)

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100"> 💻 8, 9번 스위치 입력    
```
esp32 s3 보드 8, 9 번핀에 스위치가 연결되어 있습니다. 스위치를 누르면 시리얼포트로 이를 알려줘
```
<br>     
<details>
    <summary>💻 아두이노 프로그램 </summary>

```c
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
</details>

💡  왜 Pull-up / Pull-down 이 필요한가?
디지털 입력 핀(GPIO)이 **떠 있는 상태(floating)**이면 전압이 불안정해서
- HIGH인지 LOW인지 알 수 없음
- 노이즈에 따라 상태가 불규칙하게 바뀜
- 오동작 가능성 있음
그래서 입력 핀에 기본값을 주는 회로가 필요합니다.
그게 바로 Pull-up / Pull-down 저항입니다.

💡  Pull-up / Pull-down의 차이
| 이름            | 기본 상태 | 스위치 누르면 | 설명                                     |
| ------------- | ----- | ------- | -------------------------------------- |
| **Pull-up**   | HIGH  | LOW     | 내부에서 Vcc(3.3V)에 연결됨. 스위치를 누르면 GND로 떨어짐 |
| **Pull-down** | LOW   | HIGH    | 내부에서 GND에 연결됨. 스위치를 누르면 Vcc로 올라감       |

💡 실제 프로젝트에서 추천
| 연결 방식        | 권장 설정               | 이유                |
| ------------ | ------------------- | ----------------- |
| 스위치를 GND에 연결 | `INPUT_PULLUP` 사용   | 노이즈에 강하고 안전한 방식   |
| 스위치를 Vcc에 연결 | `INPUT_PULLDOWN` 사용 | 드뭄, 일부 상황에서 사용 가능 |


🔗 [▶️ 유튜브 보기 - **IoT 스위치 만들기**](https://youtu.be/7TIiey674zA)

-------------------------------------------------------------------------

## 📌 5.3 아나로그 입력 (1 번핀)
🔗 [▶️ 유튜브 보기 - **Antigravity IoT 아두이노 보드 아나로그 입력**](https://youtu.be/o4VF_i8oHuc)
ESP32-S3 보드의 1번 핀에 아날로그 입력이 연결하여 해당 값을 읽어서 시리얼 포트로 출력하는 Arduino 프로그램입니다.
<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100"> 💻 1번 아나로그 입력    
```
https://github.com/kdi6033 i2r-05 보드 1 번핀에 아나로그 입력이 연결되어 있습니다. 입력 값을 시리얼포트로 알려줘
```
- ANALOG_PIN은 1번 핀으로 설정하여 ADC1 채널을 사용합니다.
- analogReadResolution(12)를 사용하여 아날로그 입력 값을 **12비트 해상도(0 ~ 4095)**로 읽습니다. 기본값은 12비트입니다.
- analogRead(ANALOG_PIN) 함수로 아날로그 값을 읽습니다. 읽은 값은 0에서 4095 범위의 정수로 반환됩니다.

<br>     
<details>
    <summary>💻 아두이노 프로그램 </summary>

```c
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
</details>

## 📌 5.4 Buzzer 출력 (11 번핀)

🔗 [▶️ 유튜브 보기 - **Antigravity IoT 아두이노 보드 Buzzer 출력**](https://youtube.com/shorts/og0Jyk87y6g)

ESP32-S3 보드의 11번 핀에 연결된 부저를 제어하기 위해 Arduino 코드를 작성했습니다. 부저는 PWM 신호를 통해 제어되며, 이를 통해 다양한 음을 생성할 수 있습니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  11번 Buzzer 출력    
```
https://github.com/kdi6033 i2r-05 보드 11 번핀에 Buzzer가 연결되어 있습니다. 음악연주하는 프로그램 만들어줘
```

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  음악연주   
```
부져로 음악연주하는 프로그램 만들어줘
```
ESP32-S3의 부저를 사용해 간단한 음악을 연주하는 프로그램을 작성할 수 있습니다. 아래는 아두이노의 tone() 함수를 사용하여 **"Twinkle Twinkle Little Star"**를 연주하는 예제입니다. 

<br>     
<details>
    <summary>💻 아두이노 프로그램 </summary>

```c
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
</details>

<br>     
<details>
    <summary>💻 아두이노 프로그램 슈퍼마리오 </summary>

```c
/*
  i2r-05 Buzzer Music Example
  Pin 11 is connected to the buzzer.
*/

#include "pitches.h"

#define BUZZER_PIN 11
#define REST 0

// Tempo changes the speed of the song. Higher is faster.
int tempo = 200;

// Melody: Super Mario Bros Theme
// Format: Note, Duration (4 = quarter, 8 = eighth, 12 = dotted eighth, etc.)
// Negative duration indicates a dotted note (e.g. -4 means dotted quarter note)
int melody[] = {
  NOTE_E5,8, NOTE_E5,8, REST,8, NOTE_E5,8, REST,8, NOTE_C5,8, NOTE_E5,8, REST,8,
  NOTE_G5,4, REST,4, NOTE_G4,8, REST,4, 
  NOTE_C5,4, NOTE_G4,8, REST,4, NOTE_E4,4,
  NOTE_A4,4, NOTE_B4,4, NOTE_AS4,8, NOTE_A4,4,
  NOTE_G4,8, NOTE_E5,8, NOTE_G5,8, NOTE_A5,4, NOTE_F5,8, NOTE_G5,8,
  REST,8, NOTE_E5,4, NOTE_C5,8, NOTE_D5,8, NOTE_B4,4,
  REST,4
};

// Calculate the number of notes (array size / 2 because each note has pitch + duration)
int notes = sizeof(melody) / sizeof(melody[0]) / 2;

void setup() {
  pinMode(BUZZER_PIN, OUTPUT);
}

void loop() {
  // Parsing the melody array
  for (int i = 0; i < notes * 2; i = i + 2) {

    // First element in the pair is the note
    int note = melody[i];
    // Second element in the pair is the duration
    int divider = melody[i + 1];
    
    // Calculate the duration of the note in ms
    // wholenote (in ms) = (60000 * 4) / tempo
    int noteDuration = 0;
    int wholenote = (60000 * 4) / tempo;
    
    if (divider > 0) {
      // regular note, just divide
      noteDuration = (wholenote) / divider;
    } else if (divider < 0) {
      // dotted notes are represented with negative duration
      noteDuration = (wholenote) / abs(divider);
      noteDuration *= 1.5; // increases the duration in half for dotted notes
    }

    // We only play the note for 90% of the duration, leaving 10% as a pause
    if (note != REST) {
      tone(BUZZER_PIN, note, noteDuration * 0.9);
    }
    
    // Wait for the specific duration before playing the next note.
    delay(noteDuration);
    
    // Stop the waveform generation before the next note.
    noTone(BUZZER_PIN);
  }
  
  // Wait a few seconds before replaying
  delay(2000);
}

```
</details>

<br>     
<details>
    <summary>💻 아두이노 프로그램 pitches.h </summary>

```c

/*************************************************
 * Public Constants
 *************************************************/

#define NOTE_B0  31
#define NOTE_C1  33
#define NOTE_CS1 35
#define NOTE_D1  37
#define NOTE_DS1 39
#define NOTE_E1  41
#define NOTE_F1  44
#define NOTE_FS1 46
#define NOTE_G1  49
#define NOTE_GS1 52
#define NOTE_A1  55
#define NOTE_AS1 58
#define NOTE_B1  62
#define NOTE_C2  65
#define NOTE_CS2 69
#define NOTE_D2  73
#define NOTE_DS2 78
#define NOTE_E2  82
#define NOTE_F2  87
#define NOTE_FS2 93
#define NOTE_G2  98
#define NOTE_GS2 104
#define NOTE_A2  110
#define NOTE_AS2 117
#define NOTE_B2  123
#define NOTE_C3  131
#define NOTE_CS3 139
#define NOTE_D3  147
#define NOTE_DS3 156
#define NOTE_E3  165
#define NOTE_F3  175
#define NOTE_FS3 185
#define NOTE_G3  196
#define NOTE_GS3 208
#define NOTE_A3  220
#define NOTE_AS3 233
#define NOTE_B3  247
#define NOTE_C4  262
#define NOTE_CS4 277
#define NOTE_D4  294
#define NOTE_DS4 311
#define NOTE_E4  330
#define NOTE_F4  349
#define NOTE_FS4 370
#define NOTE_G4  392
#define NOTE_GS4 415
#define NOTE_A4  440
#define NOTE_AS4 466
#define NOTE_B4  494
#define NOTE_C5  523
#define NOTE_CS5 554
#define NOTE_D5  587
#define NOTE_DS5 622
#define NOTE_E5  659
#define NOTE_F5  698
#define NOTE_FS5 740
#define NOTE_G5  784
#define NOTE_GS5 831
#define NOTE_A5  880
#define NOTE_AS5 932
#define NOTE_B5  988
#define NOTE_C6  1047
#define NOTE_CS6 1109
#define NOTE_D6  1175
#define NOTE_DS6 1245
#define NOTE_E6  1319
#define NOTE_F6  1397
#define NOTE_FS6 1480
#define NOTE_G6  1568
#define NOTE_GS6 1661
#define NOTE_A6  1760
#define NOTE_AS6 1865
#define NOTE_B6  1976
#define NOTE_C7  2093
#define NOTE_CS7 2217
#define NOTE_D7  2349
#define NOTE_DS7 2489
#define NOTE_E7  2637
#define NOTE_F7  2794
#define NOTE_FS7 2960
#define NOTE_G7  3136
#define NOTE_GS7 3322
#define NOTE_A7  3520
#define NOTE_AS7 3729
#define NOTE_B7  3951
#define NOTE_C8  4186
#define NOTE_CS8 4435
#define NOTE_D8  4699
#define NOTE_DS8 4978
```
</details>


[Buzzer 음악 제작 참조사이트](https://github.com/robsoncouto/arduino-songs/tree/master)

🔗 [▶️ 유튜브 보기 - **🤖🎶 Gemini Antigravity: AI와 함께하는 아두이노 음악 연주 프로그램**](https://youtube.com/shorts/t_A86b2qr3I)

[Buzzer 참조할 만한 추천 사이트](https://github.com/robsoncouto/arduino-songs/tree/master) 

## 📌 5.5 Light 센서 (2 번핀)

ESP32-S3 보드의 11번 핀에 연결된 부저를 제어하기 위해 Arduino 코드를 작성했습니다. 부저는 PWM 신호를 통해 제어되며, 이를 통해 다양한 음을 생성할 수 있습니다.    

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  Light 센서
```
https://github.com/kdi6033 i2r-05 보드 2 번핀에 Light 센서가 연결되어 있습니다. 조도를 출력하는 프로그램해줘
```
- LIGHT_SENSOR_PIN 설정: 센서가 연결된 핀 번호를 #define으로 정의합니다.
- analogReadResolution(12): ESP32-S3의 ADC는 최대 12비트 해상도를 지원합니다. 이를 설정해 ADC 값이 0~4095 범위로 출력되도록 합니다.
- Serial 출력: 읽은 ADC 값과 전압 값을 시리얼 모니터에 출력합니다

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
const int lightSensorPin = 2; // 조도 센서 핀 (Pin 2)

void setup() {
  Serial.begin(115200); // 시리얼 통신 초기화
  pinMode(lightSensorPin, INPUT); // 핀 모드 설정
}

void loop() {
  int sensorValue = analogRead(lightSensorPin); // 조도 센서 값 읽기 (0 ~ 4095)
  
  Serial.print("Illuminance Value: ");
  Serial.println(sensorValue); // 시리얼 모니터에 출력
  
  delay(500); // 0.5초 대기
}
```
</details>


## 📌 5.6 DHT11 온습도 센서 (10 번핀)

이 프로그램은 DHT 라이브러리를 사용하여 온도와 습도를 읽고 시리얼 모니터에 출력합니다.   

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  DHT11 온습도 센서
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

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
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
</details>

🔗 [Buzzer 음악 만들기 참조 사이트](https://github.com/robsoncouto/arduino-songs/tree/master)

## 📌 5.7 LM35 온도 센서 (4 번핀)

LM35 온도 센서는 아날로그 출력 타입의 온도 센서입니다. 온도를 섭씨(°C)로 측정하며, 출력 전압은 섭씨 1도당 10mV입니다. 이를 ESP32-S3의 4번 핀에 연결하여 값을 읽고 온도를 출력하는 프로그램은 다음과 같이 작성할 수 있습니다.


🔗 [▶️ 유튜브 보기 - **🤖🎶 Gemini Antigravity: AI와 함께하는 LM35 온도 센서 프로그램**](https://youtube.com/shorts/PyqmXhaykfk)

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  LM35 온도 센서
```
https://github.com/kdi6033 i2r-05 보드 LM35 센서가 4번핀에 연결되어 있어요 프로그램 해주세요
```

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
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
</details>

## 📌 5.8 RGB Led 센서 (15,21,16 번핀 red,green,blue)

이 프로그램은 RGB LED의 각 핀에 대해 LED의 밝기를 제어합니다. 빨강, 초록, 파랑, 흰색의 조합을 통해 다양한 색상을 순차적으로 출력합니다.

<img src="https://github.com/user-attachments/assets/8d3ef6cc-9df4-47de-a5eb-6bd3402c9eb4" alt="chatGPT" width="100">  RGB Led 센서
```
https://github.com/kdi6033 i2r-05 보드 15,21,16 이 차례로 red, green, blue 가 연결되어 있습니다. led 프로그램 해줘
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

----

## ✅ 7. 온도  습도 센서  (i2r-06)

🎯 개요
SHT30은 Sensirion의 **SHT3X 시리즈 디지털 온습도 센서**로,  
**I²C 통신**을 사용하여 온도와 습도를 정밀하게 측정할 수 있습니다.  
ESP32, 아두이노 기반 **IoT PLC 및 환경 모니터링 시스템**에 적합합니다.

🤖 Claude Code 사용 Physical AI i2r-06 자동 프로그램
```
https://github.com/kdi6033/i2r-05/blob/main/CLAUDE.md
읽고 [원하는 동작을 한국어로 설명]
```

---

🎯 주요 사양

- 전원 전압: **2.4V ~ 5.5V**
- 통신 방식: **I²C** (Address 0x44)
- 온도 정확도: **±0.3°C**
- 습도 정확도: **±3.0%RH**
- 온도 측정 범위: **-40°C ~ 125°C**
- 습도 측정 범위: **0 ~ 100%RH**
- 해상도: **0.1°C / 0.1%RH**

---

🎯 배선 색상

| 선 색상 | 기능 | i2r-05 핀번호 |
|--------|------|------|
| **갈색** | VCC (전원) | 5V |
| **블랙** | GND (접지) | GND |
| **노랑** | SCL (I²C 클럭) | 17 |
| **파랑** | SDA (I²C 데이터) | 18 |

---

🎯 활용 예

- ESP32 기반 IoT PLC 온습도 측정  
- MQTT 클라우드 환경 모니터링  
- 스마트팜 / 공장 환경 센싱

-----

<img src="https://github.com/kdi6033/i2r-05/blob/main/images/i2r-06-circut.png?raw=true" height="240">

<br>     
<details>
    <summary>💻 아두이노 온도 습도 측정 프로그램</summary>

```c
#include <Wire.h>

// SHT30 I2C 주소 (기본값: 0x44, 설정에 따라 0x45일 수 있음)
#define SHT30_ADDRESS 0x44

// i2r-05 핀 설정
#define SDA_PIN 18
#define SCL_PIN 17

void setup() {
  Serial.begin(115200);
  while (!Serial); // 시리얼 모니터 연결 대기

  // I2C 초기화 (SDA, SCL)
  Wire.begin(SDA_PIN, SCL_PIN);
  
  Serial.println("SHT30 온습도 센서 테스트 시작...");
}

void loop() {
  // 측정 명령 전송 (High repeatability, Clock stretching disabled: 0x2C06)
  Wire.beginTransmission(SHT30_ADDRESS);
  Wire.write(0x2C);
  Wire.write(0x06);
  byte error = Wire.endTransmission();

  if (error != 0) {
    Serial.println("SHT30 센서를 찾을 수 없습니다. 연결을 확인하세요.");
    delay(2000);
    return;
  }

  // 측정 시간 대기 (0x2C06 모드는 변환 시간이 필요함)
  delay(50); 

  // 데이터 요청 (6바이트: 온도 MSB, LSB, CRC, 습도 MSB, LSB, CRC)
  Wire.requestFrom(SHT30_ADDRESS, 6);

  if (Wire.available() == 6) {
    // 온도 데이터 읽기
    uint16_t tempRaw = (Wire.read() << 8) | Wire.read();
    uint8_t tempCrc = Wire.read(); // CRC 무시

    // 습도 데이터 읽기
    uint16_t humiRaw = (Wire.read() << 8) | Wire.read();
    uint8_t humiCrc = Wire.read(); // CRC 무시

    // 온도 계산 공식: -45 + 175 * (S_T / 2^16 - 1)
    float temperature = -45 + (175 * ((float)tempRaw / 65535.0));

    // 습도 계산 공식: 100 * (S_RH / 2^16 - 1)
    float humidity = 100 * ((float)humiRaw / 65535.0);

    // 결과 출력
    Serial.print("온도: ");
    Serial.print(temperature, 1);
    Serial.print(" °C \t");
    Serial.print("습도: ");
    Serial.print(humidity, 1);
    Serial.println(" %RH");
  } else {
    Serial.println("데이터 수신 실패");
  }

  delay(2000); // 2초마다 측정
}

```
</details>

🎯 온도 습도를 Oled에 표시하는 프로그램


<br>     
<details>
    <summary>💻 아두이노 온도 습도 Oled에 모니터링 프로그램</summary>

```c
#include <Arduino.h>
#include <U8g2lib.h>
#include <Wire.h>

// 1. SHT30 설정
#define SHT30_ADDRESS 0x44

// 2. LCD 설정 (1.3인치 SH1106 I2C OLED, SCL=17, SDA=18)
// U8g2 하드웨어 I2C 생성자 (회전, 리셋, SCL, SDA)
U8G2_SH1106_128X64_NONAME_F_HW_I2C u8g2(U8G2_R0, U8X8_PIN_NONE, 17, 18);

// 3. 아이콘 비트맵 데이터
// Bluetooth 아이콘 (9x13)
const unsigned char bt_icon[] U8X8_PROGMEM = {
  0x08, 0x00, 0x18, 0x00, 0x28, 0x00, 0x48, 0x00,
  0x88, 0x00, 0x50, 0x00, 0x20, 0x00, 0x50, 0x00,
  0x88, 0x00, 0x48, 0x00, 0x28, 0x00, 0x18, 0x00, 0x08, 0x00
};

// Rounder Wifi Icon (16x13)
const unsigned char wifi_rounder[] U8X8_PROGMEM = {
  0x00, 0x00, 
  0xF0, 0x0F, // ....########....
  0x0C, 0x30, // ..##........##..
  0x02, 0x40, // .#............#.
  0x00, 0x00, // ................
  0xE0, 0x07, // .....######.....
  0x18, 0x18, // ...##......##...
  0x00, 0x00, // ................
  0xC0, 0x03, // ......####......
  0x20, 0x04, // .....#....#.....
  0x00, 0x00, // ................
  0x80, 0x01, // .......##.......
  0x80, 0x01, // .......##.......
};

// 전역 변수
float temperature = 0.0;
float humidity = 0.0;
unsigned long lastMeasureTime = 0;
const long interval = 2000; // 2초 간격 측정

void setup(void) {
  Serial.begin(115200);
  
  // U8g2 초기화 (내부적으로 Wire.begin(18, 17)을 처리함)
  u8g2.begin();
  u8g2.enableUTF8Print(); 
  
  Serial.println("System Initialized");
}

void loop(void) {
  unsigned long currentMillis = millis();

  // 2초마다 센서 데이터 갱신
  if (currentMillis - lastMeasureTime >= interval) {
    lastMeasureTime = currentMillis;
    readSHT30();
  }

  u8g2.clearBuffer();

  // 1. 텍스트 출력 (한글)
  // '온' 글자가 korean1에 누락될 수 있으므로 korean2 사용
  u8g2.setFont(u8g2_font_unifont_t_korean2); 
  
  // 온도 표시 (화면 잘림 방지 여백 추가)
  u8g2.setCursor(5, 20);
  u8g2.print("온도 : ");
  u8g2.print(temperature, 1);
  u8g2.print(" °C");

  // 습도 표시
  u8g2.setCursor(5, 40);
  u8g2.print("습도 : ");
  u8g2.print(humidity, 1);
  u8g2.print(" %");

  // 2. 하단 아이콘 (WiFi, BT) - 하단 배치 (Y ~ 64)
  // 화면 높이 64, 아이콘 높이 13 -> y = 64-13 = 51 (여유있게 50)
  
  // WiFi 아이콘 (우측 하단 끝 쯤)
  // X = 128 - 16(width) - 10(margin) = 102
  u8g2.drawXBM(102, 50, 16, 13, wifi_rounder);
  
  // Bluetooth 아이콘 (Wifi 옆)
  // X = 102 - 9(width) - 10(margin) = 83
  u8g2.drawXBM(83, 51, 9, 13, bt_icon); 

  // 하단 상태 텍스트 (옵션)
  u8g2.setFont(u8g2_font_t0_11_tf); // 작은 영문 폰트
  u8g2.setCursor(0, 60);
  u8g2.print("Monitor");

  u8g2.sendBuffer();
}

void readSHT30() {
  // 측정 명령 전송
  Wire.beginTransmission(SHT30_ADDRESS);
  Wire.write(0x2C);
  Wire.write(0x06);
  if (Wire.endTransmission() != 0) {
    Serial.println("SHT30 Error");
    return;
  }

  // 데이터 시트상 측정 대기 시간 필요
  delay(50); 

  Wire.requestFrom(SHT30_ADDRESS, 6);

  if (Wire.available() == 6) {
    uint16_t tempRaw = (Wire.read() << 8) | Wire.read();
    Wire.read(); // CRC
    uint16_t humiRaw = (Wire.read() << 8) | Wire.read();
    Wire.read(); // CRC

    temperature = -45 + (175 * ((float)tempRaw / 65535.0));
    humidity = 100 * ((float)humiRaw / 65535.0);
    
    Serial.print("T: "); Serial.print(temperature);
    Serial.print(" H: "); Serial.println(humidity);
  }
}

```
</details>


---


## ✅ 7. Otto Ninja 로봇
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

💻 LL 360 서보모터 속도 조절 원리

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

💻 로봇 속도 조절 전후진 프로그램
- 서보모터는 1500us 기준으로 속도와 방향을 제어합니다
- 속도는 1500이면 정지하고 이보다 작으면 역회전 이보다 크면 정회전 합니다.
- 속도가 너무 낮거나 너무 높으면 동작 불안정 또는 고장 위험
- 안정적인 동작을 위해 1500을 기준으로 위야래 100~300으로 제한하는 것이 좋음
- constrain() 함수로 속도를 자동 보정하면 사용자 실수 방지 가능
  
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
void moveForward(int speed) {
  speed = constrain(speed, 100, 300); // 권장 범위 자동 보정
  int pulse = 1500 + speed;
  servoLL.writeMicroseconds(pulse);
  servoRL.writeMicroseconds(1500 - speed); // 반대방향 회전
  Serial.print("▶ 전진 (보정된 속도): "); Serial.println(speed);
}

void moveBackward(int speed) {
  speed = constrain(speed, 100, 300); // 권장 범위 자동 보정
  int pulse = 1500 - speed;
  servoLL.writeMicroseconds(pulse);
  servoRL.writeMicroseconds(1500 + speed); // 반대방향 회전
  Serial.print("◀ 후진 (보정된 속도): "); Serial.println(speed);
}

void stopMoving() {
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

  moveForward(50);   // 100으로 자동 보정됨
  delay(1000);

  stopMoving();
  delay(500);

  moveBackward(400); // 300으로 자동 보정됨
  delay(1000);

  stopMoving();
  delay(500);
  
}

void loop() {

}
```

💻 MQTT 통신에 의한 전진 후진 통신 프로그램
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
💻 LL 모터만 전후진 아두이노 프로그램
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

💻 LL RL 모터 전후진 아두이노 프로그램
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

## ✅ 8. 1.3" OLED LCD 128x64
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

✅ 눈동자 움직이는 그래픽 프로그램
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

✅ 무지개 🌈 / 점멸 ✨ / 흐름 💨
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

## ✅ 9.  VL53L0X Time-of-Flight (ToF) 거리 센서
<img src="https://github.com/user-attachments/assets/1e3b3bde-cb82-42ad-af43-7e03a7ce1e27" alt="VL53L0X" width="300">

🔍 개요
VL53L0X는 STMicroelectronics에서 개발한 **레이저 기반 Time-of-Flight(ToF) 거리 센서**입니다.  
적외선 레이저 펄스를 발사하고 반사되는 시간을 측정하여 **매우 정확한 거리**를 측정할 수 있습니다.  
광량, 반사율, 색상에 크게 영향을 받지 않아 안정적인 측정이 가능하며, 소형 폼팩터로 IoT, 로봇, HMI 등에 적합합니다.

---

📖 주요 사양

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

⚙️ 핀 설명 (보드에 따라 다름)

| 핀 이름 | 기능 설명                                      |
|---------|------------------------------------------------|
| VIN     | 전원 입력 (3.3V 또는 5V)                        |
| GND     | 접지                                           |
| SDA     | I2C 데이터                                     |
| SCL     | I2C 클럭                                       |
| XSHUT   | 전원 제어 (여러 센서 사용 시 주소 설정에 활용) |
| GPIO1   | 인터럽트 출력 (일반적으로 사용하지 않음)       |

---

🧩 응용 분야
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

💻 통합 프로그램: OLED 눈 + LED 효과 + 거리 측정 출력 (Serial)
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

---

-----------
## ✅ 10. 조도센서 (GY302)
🔗 [📺 영상 보기 - **AI IoT 아두이노 보드 조도센서 **](https://youtu.be/GoVdq9TUvuM)

i2r‑05 보드의 I2C 핀(GPIO17=SCL, GPIO18=SDA) 에 연결된 GY‑302 (BH1750) 조도 센서용 아두이노 프로그램 입니다.
- GY-320은 GY-302의 오기일 가능성이 높으며, 실제 센서는 BH1750을 사용합니다.
- 해당 센서는 I2C 통신 방식이며, i2r‑05 보드의 핀맵에 따라 다음처럼 연결합니다:

📦 설치 라이브러리
- Arduino IDE에서 BH1750 by Christopher Laws 설치:
- Arduino IDE → 라이브러리 매니저 → BH1750 → 설치

| BH1750 (GY-302) 핀 | i2r‑05 GPIO | 설명              |
| ----------------- | ----------- | --------------- |
| VCC               | 3.3V 또는 5V  | 전원 공급           |
| GND               | GND         | 공통 접지           |
| SDA               | IO18        | I2C 데이터         |
| SCL               | IO17        | I2C 클럭          |
| ADDR              | GND (or NC) | 주소 설정 (기본 0x23) |

💻 조도센서 GY-302 프로그램
```
#include <Wire.h>
#include <BH1750.h>

BH1750 lightMeter;

void setup() {
  Serial.begin(115200);

  // I2C 핀 설정 (SDA=18, SCL=17) — i2r-05 보드 전용
  Wire.begin(18, 17);

  // BH1750 초기화
  if (lightMeter.begin(BH1750::CONTINUOUS_HIGH_RES_MODE)) {
    Serial.println("✅ BH1750 시작 성공!");
  } else {
    Serial.println("❌ BH1750 초기화 실패. 연결 확인!");
    while (1);
  }
}

void loop() {
  float lux = lightMeter.readLightLevel();
  Serial.print("💡 조도: ");
  Serial.print(lux);
  Serial.println(" lux");

  delay(1000);  // 1초 간격
}
```

📌 참고 사항    
- 주소 변경: GY-302 센서에서 ADDR 핀을 GND에 연결하면 주소는 0x23, VCC에 연결하면 0x5C입니다. 대부분 GND 또는 미연결(기본 0x23)로 사용됩니다.
- 조도 범위: 약 1~65535 lux까지 측정 가능.

-----------------------------------------------------------------
## ✅ 11. ESP32 S3 AI IoT  아두이노보드 크라우드 연결 및 개요요
ESP32는 Bluetooth Classic과 Bluetooth Low Energy(BLE)를 모두 지원하는 강력한 무선 모듈입니다.
BLE는 저전력으로 데이터를 전송할 수 있어, IoT(사물인터넷) 기기에서 널리 사용됩니다.
블루투스는 스마트폰의 블루투스와 연결하여 와이파이 정보를 보드로 전송하여 통신 접속을 하게 합니다. 

🔗 [📺 영상 보기 - **AI IoT 아두이노 보드 와이파이, 크라우드 연결**](https://youtu.be/R9wEoO4aQpU)

> 🧠 이 영상에서는 **i2r-05 AI IoT 보드**를 Wi-Fi 및 클라우드에 연결하는 방법을 자세히 설명합니다.
> - 📡 와이파이 설정 방법
> - ☁️ 크라우드 연동 방법
> - 📱 웹앱 접속 및 제어 방법

| 상태           | LED 색상 | 설명                       |
| ------------ | ------ | ------------------------ |
| 🔴 연결되지 않음   | 빨간색    | Wi-Fi 또는 MQTT 서버에 연결 안 됨 |
| 🟢 연결 성공     | 초록색    | 와이파이, mqtt 서버에 연결됨        |
| 🔵 블루투스 연결 중 | 파란색    | 블루투스 통신 중, 와이파이 정보 입력과 제어용으로 사용 |
| 🟡 펌웨어 다운로드 중   | 노란색    | 보드의새로운 펌웨어 다운로드 중  |



🔗 [▶️ 유튜브 보기 - **AI IoT 아두이노 보드 웹앱 사용법**](https://youtu.be/R9wEoO4aQpU)

> 크라우드에 접속하여 스위치, 온도, 습도, 아나로그 센서, 조도센서 등을 원격으로 모니터링 제어 하는 방법을 소개한다.

<br>     
<details>
    <summary>💻 아두이노 프로그램</summary>

```c
  ✅ 프로그램
```
</details>

--------------------

✅ 과목 문단명
▶️[유튜브] 유튜브
📌🔰 개요 및 준비
🎯 학습 목표 및 기대 효과
📋 요약 / 정리 / 확장 학습
⚙️ 개발 환경 및 준비물
🚀 실행, 런칭
🟢	시작 신호 (녹색: 실행 의미)
📦  필요 라이브러리 설치 방법 
💻 소프트웨어 
🔍	결과 확인, 테스트
🔗 링크
🌐 확장 기능 (통신)
📚 참고 자료 및 링크
💡	팁 / 확장 아이디어
🧠 학생 과제 또는 연습 문제
🤖	로봇 프로젝트 / 자율 동작 시스템


