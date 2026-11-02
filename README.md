# 디스코드 퀘스트 자동화 완벽 매뉴얼 / Discord Quests Automation Manual

> **[저작권 및 공식 채널 안내 / Copyright & Notice]**
> - **저작권자 / Author**: 비가드 (Bigad)
> - **무단 배포 및 2차 수정 금지** (Unauthorized redistribution and modification strictly prohibited)
> - **공식 유튜브 채널 / Official Channel**: [https://www.youtube.com/@Bigad2007](https://www.youtube.com/@Bigad2007)

---

## 📌 빠른 이동 목차 (Quick Navigation)

- [🇰🇷 한국어 매뉴얼](#-한국어-매뉴얼-korean-guide)
  - [1. 웹사이트 vs 데스크톱 앱 차이 한눈에 보기](#1-웹사이트-vs-데스크톱-앱-차이-한눈에-보기)
  - [2. 필수 사전 작업: 콘솔 붙여넣기 잠금 해제](#2-필수-사전-작업-콘솔-붙여넣기-잠금-해제-allow-pasting)
  - [3. [웹사이트 전용] 동영상 퀘스트 완료 가이드](#3-웹사이트-전용-동영상-퀘스트-완료-가이드-웹-브라우저)
  - [4. [데스크톱 앱 전용] 게임 플레이 포함 모든 퀘스트 완료 가이드](#4-데스크톱-앱-전용-게임-플레이-포함-모든-퀘스트-완료-가이드-설치형-앱)
  - [5. 대시보드 조작법 및 단축키](#5-대시보드-조작법-및-단축키)
- [🇺🇸 English Guide](#-english-guide-영어-매뉴얼)
  - [1. Comparison: Web Browser vs Desktop App](#1-comparison-web-browser-vs-desktop-app)
  - [2. Prerequisite: Unlock Console Pasting](#2-prerequisite-unlock-console-pasting-allow-pasting)
  - [3. [Web Browser Only] Video Quests Guide](#3-web-browser-only-video-quests-guide)
  - [4. [Desktop App Only] All Quests (Game Play & Stream) Guide](#4-desktop-app-only-all-quests-game-play--stream-guide)
  - [5. Controls & Shortcuts](#5-controls--shortcuts)

---

## 🇰🇷 한국어 매뉴얼 (Korean Guide)

### 1. 웹사이트 vs 데스크톱 앱 차이 한눈에 보기

디스코드는 브라우저(웹사이트)와 설치형 프로그램(앱)의 권한 구조가 완전히 다릅니다.

| 항목 | 🌐 웹사이트 (Chrome, Safari, Edge 등) | 💻 데스크톱 앱 (Mac / Windows 설치형) |
| :--- | :--- | :--- |
| **완료 가능한 퀘스트** | • **동영상 시청 퀘스트** (`WATCH_VIDEO`) | • **모든 퀘스트 지원** (동영상 + 게임 플레이 + 스트리밍) |
| **진행 불가 퀘스트** | • **게임 15분 플레이** (`GAME`)<br>• **화면 공유 방송** (`STREAM`) | **없음 (모두 정상 작동)** |
| **차이가 나는 이유** | 브라우저 보안 정책상 컴퓨터 내부에서 어떤 프로그램이 실행 중인지 읽을 수 없습니다. | 디스코드 자체 모듈(`DiscordNative`)을 제어하여 실제 게임이 켜진 것처럼 신호를 보낼 수 있습니다. |
| **추천 사용 대상** | 설치 없이 트레일러/영상 퀘스트만 10초 만에 끝내고 싶을 때 | 파이어폭스, 엔드필드 등 대형 게임 플레이 퀘스트를 깨야 할 때 |

---

### 2. 필수 사전 작업: 콘솔 붙여넣기 잠금 해제 (`allow pasting`)

디스코드 콘솔창에 코드를 붙여넣으려고 할 때 **빨간색 경고문이 뜨며 작성이 안 되는 경우**, 아래 순서대로 보안 잠금을 풀어주어야 합니다.

1. 개발자 도구의 **[Console]** 창 맨 아래 텍스트 입력 줄(`>`)을 마우스로 클릭합니다.
2. 따옴표 없이 아래 명령어를 그대로 타이핑합니다:
   ```text
   allow pasting
   ```
3. 키보드 **Enter**를 누릅니다.
4. 이제 차단이 풀리며 스크립트 코드를 자유롭게 붙여넣기(`Cmd + V` 또는 `Ctrl + V`)할 수 있습니다.

---

### 3. [웹사이트 전용] 동영상 퀘스트 완료 가이드 (웹 브라우저)

> **안내**: 웹사이트에서는 메이플스토리, 멜론 샌드박스 등 **동영상 시청 퀘스트만 진행**됩니다. (게임 플레이 퀘스트는 자동으로 건너뜁니다.)

1. **웹 브라우저 열기**: 크롬 또는 사파리로 [디스코드 웹사이트](https://discord.com/app)에 접속하여 로그인합니다.
2. **개발자 도구 실행**: 키보드 단축키를 누릅니다.
   - Mac: `Option + Command + I`
   - Windows: `F12` 또는 `Ctrl + Shift + I`
3. **콘솔 탭 이동**: 상단 메뉴 중 **[Console]** 탭을 클릭합니다.
4. **잠금 확인**: 붙여넣기가 안 될 경우 위의 [2번 항목](#2-필수-사전-작업-콘솔-붙여넣기-잠금-해제-allow-pasting)을 참고해 `allow pasting`을 입력합니다.
5. **스크립트 붙여넣기**: Orion 자동화 스크립트 코드를 복사한 뒤 콘솔창에 붙여넣고 **Enter**를 누릅니다.
6. **언어 선택**: 화면 중앙 팝업에서 **[한국어]** 버튼을 클릭합니다.
7. **퀘스트 진행**: 대시보드가 뜨면 영상 퀘스트가 체크되어 있는지 확인하고 **[시작]**을 누릅니다. 몇 초 만에 완료됩니다.

---

### 4. [데스크톱 앱 전용] 게임 플레이 포함 모든 퀘스트 완료 가이드 (설치형 앱)

> **안내**: 파이어폭스 15분 사용, 엔드필드 15분 플레이 등 **PC 전용 게임 퀘스트까지 전부 완료**하려면 반드시 이 방식으로 진행해야 합니다.

#### 1단계: Mac 데스크톱 앱 개발자 도구 활성화 (최초 1회만 진행)
디스코드 데스크톱 앱은 기본적으로 콘솔 단축키가 꺼져 있으므로 설정 파일을 열어주어야 합니다.
1. `Cmd + Space`를 눌러 **터미널(Terminal)**을 검색해 실행합니다.
2. 아래 명령어를 그대로 복사하여 터미널에 붙여넣고 **Enter**를 누릅니다:
   ```bash
   mkdir -p ~/Library/Application\ Support/discord && echo '{"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOU_ARE_DOING": true}' > ~/Library/Application\ Support/discord/settings.json
   ```
3. 현재 켜져 있는 **디스코드 데스크톱 앱을 완전히 종료(Cmd + Q)한 뒤 다시 실행**합니다.

#### 2단계: 스크립트 실행 및 퀘스트 올클리어
1. **디스코드 앱 클릭**: 디스코드 화면 아무 곳이나 클릭해 활성화합니다.
2. **개발자 도구 열기**: `Option + Command + I` 단축키를 누르면 우측에 개발자 도구가 나타납니다.
3. **콘솔 이동**: 상단에서 **[Console]** 탭을 클릭합니다.
4. **입력 잠금 해제**: 빨간 경고창이 뜨면 `allow pasting` 입력 후 Enter를 누릅니다.
5. **코드 실행**: 스크립트를 붙여넣고 Enter를 칩니다.
6. **언어 선택**: 화면 가운데 팝업에서 **[한국어]**를 선택합니다.
7. **퀘스트 확인**: 웹에서는 보이지 않던 게임 플레이 퀘스트들이 목록에 전부 체크되어 나타납니다.
8. **시작 및 수령**:
   - **[시작]** 버튼을 누르면 가짜 프로세스를 생성해 퀘스트 목표 시간을 채웁니다.
   - 100%가 완료되면 우측의 **[보상 수령]** 버튼을 눌러 오브(Orbs)와 아이템을 획득합니다.

---

### 5. 대시보드 조작법 및 단축키

- **UI 숨기기 / 다시 열기**: 키보드 `Shift + .` 또는 `>`
- **대시보드 접기/펼치기**: 상단 제목 표시줄(헤더) **더블 클릭**
- **대시보드 위치 이동**: 상단 제목 표시줄을 클릭한 채 **마우스 드래그**
- **스크립트 강제 중지**: 상단 우측 빨간색 **[중지]** 버튼 클릭

---
[맨 위로 이동 (Back to Top)](#디스코드-퀘스트-자동화-완벽-매뉴얼--discord-quests-automation-manual)
---

## 🇺🇸 English Guide (영어 매뉴얼)

### 1. Comparison: Web Browser vs Desktop App

Discord enforces different security sandboxing between browsers and installed native applications.

| Feature | 🌐 Web Browser (Chrome, Safari, Edge) | 💻 Desktop App (macOS / Windows App) |
| :--- | :--- | :--- |
| **Supported Quests** | • **Video Watching Quests** (`WATCH_VIDEO`) | • **All Quest Types** (Video + Game Play + Stream) |
| **Unsupported Quests** | • **Game Play Quests** (Play 15 mins)<br>• **Go Live Streaming** (`STREAM`) | **None (Full Support)** |
| **Technical Reason** | Web browsers cannot access system-level background processes due to sandbox restrictions. | Native desktop modules (`DiscordNative`) allow injecting spoofed game heartbeats directly to Discord. |
| **Recommended For** | Users who only want to complete 1-minute video trailers. | Users who need to complete game play requirements (e.g., Firefox, Endfield). |

---

### 2. Prerequisite: Unlock Console Pasting (`allow pasting`)

If pasting is blocked with a security warning in the console:

1. Click on the input line next to the `>` sign at the bottom of the **[Console]** tab.
2. Type the following text:
   ```text
   allow pasting
   ```
3. Press **Enter**.
4. Console pasting protection is now unlocked. You can paste using `Cmd + V` (or `Ctrl + V`).

---

### 3. [Web Browser Only] Video Quests Guide

> **Note**: In a web browser, the script will only execute video trailer quests. Game play tasks will be automatically skipped.

1. **Open Discord Web**: Go to [Discord Web](https://discord.com/app) in Chrome/Safari and log in.
2. **Open DevTools**: Press the shortcut:
   - macOS: `Option + Command + I`
   - Windows: `F12` or `Ctrl + Shift + I`
3. **Switch to Console**: Click on the **[Console]** tab at the top.
4. **Unlock Pasting**: If pasting is blocked, type `allow pasting` and press Enter.
5. **Paste Script**: Copy the Orion automation code, paste it into the console, and press **Enter**.
6. **Choose Language**: Click **[English]** on the startup modal.
7. **Start**: Review your video tasks and click the green **[START]** button.

---

### 4. [Desktop App Only] All Quests (Game Play & Stream) Guide

> **Note**: Required to automate **"Play for 15 minutes"** quests such as Firefox, Endfield, and other native game tasks.

#### Step 1: Enable Desktop DevTools (One-time macOS setup)
1. Press `Cmd + Space`, search for **Terminal**, and launch it.
2. Paste the command below and press **Enter**:
   ```bash
   mkdir -p ~/Library/Application\ Support/discord && echo '{"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOU_ARE_DOING": true}' > ~/Library/Application\ Support/discord/settings.json
   ```
3. **Completely quit (Cmd + Q) and restart the Discord desktop app.**

#### Step 2: Run the Script & Complete All Tasks
1. **Focus Discord**: Click anywhere inside the Discord application.
2. **Open Console**: Press `Option + Command + I`.
3. **Go to Console Tab**: Click the **[Console]** tab.
4. **Unlock Pasting**: Type `allow pasting` and press Enter if prompted.
5. **Run Script**: Paste the script and hit **Enter**.
6. **Select Language**: Click **[English]** on the language dialog.
7. **Verify Quests**: Both Game Play and Video quests will now appear in the list.
8. **Claim Rewards**:
   - Click **[START]** to simulate background gameplay sessions.
   - Once tasks reach 100%, click the **[CLAIM REWARD]** button on each card.

---

### 5. Controls & Shortcuts

- **Toggle UI Window**: `Shift + .` or `>`
- **Collapse / Expand Dashboard**: **Double-click** the top header
- **Move Dashboard**: Click and **drag** the header bar
- **Force Stop Automation**: Click the red **[STOP]** button in the top right

---
[맨 위로 이동 (Back to Top)](#디스코드-퀘스트-자동화-완벽-매뉴얼--discord-quests-automation-manual)
