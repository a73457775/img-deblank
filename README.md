# 🎬 Image deblank

본 프로젝트는 브라우저 환경에서 작동하는 고정밀 배경 제거 및 이미지 리터칭 전문 도구입니다. 텐서플로우(TensorFlow.js)에서 시작하여 미디어파이프(MediaPipe) 기반의 최첨단 매팅 기술까지 진화해 온 과정을 담고 있습니다.

## 🚀 프로젝트 로드맵 (버전별 특징)

본 프로젝트는 단계별로 기능을 고도화하며 발전해왔습니다.

*   **V1 (Basic AI)**: `Body-Pix`를 이용한 기본적인 인물 인식 및 배경 제거.
*   **V2 (Pro Engine)**: `DeepLabV3` 모델 도입으로 20여 종의 다양한 사물을 인식 가능.
*   **V3 (Ultra Edition)**: 미세한 머리카락 디테일을 살려주는 `Guided Filter` 보정 알고리즘 및 자유로운 캔버스 이동(Pan/Zoom) 시스템 도입.
*   **V0.5 / V5 (Latest - Professional)**: **인터랙티브 세그멘테이션(Magic Point)**, **컬러 지우개**, **스마트 브러쉬**, **실행 취소(Undo)** 기능이 통합된 전문가용 UI 버전.

---

## 🛠 주요 기술 스펙 (Specification)

*   **Core Engine**: MediaPipe Tasks Vision (DeeplabV3 & Magic Touch 모델)
*   **Edge Refinement**: Guided Filter Decomposition (테두리 정밀 복원 알고리즘)
*   **Graphics**: HTML5 Canvas API (Pixel-level manipulation)
*   **Coordinate System**: Absolute Viewport 1:1 Pixel Mapping logic (좌표 오차 0 구현)
*   **UI/UX**: CSS3 Glassmorphism 디자인, GPU 가속 애니메이션
*   **Performance**: WebGL/WASM 가속을 이용한 실시간 브라우저 연산

---

## 💡 주요 기능 및 사용법 (User Guide)

### 1. 에디터 조작 (Navigation)
*   **확대/축소**: 마우스 휠 (1% ~ 4000% 지원)
*   **화면 이동 (Panning)**: `Space` 키를 누른 채 드래그 또는 마우스 휠 클릭 드래그
*   **원본 보기**: 좌측 `👁️` 버튼을 누르고 있으면 원본 이미지가 표시됩니다.
*   **화면 맞춤**: `R` 키를 누르면 이미지가 화면 크기에 맞춰 초기화됩니다.
*   **실행 취소 (Undo)**: `Ctrl + Z`를 통해 작업 단계를 되돌릴 수 있습니다.

### 2. 편집 도구 (Tools)
*   **🎯 전체 스캔 (AI Precision Scan)**: AI가 이미지 전체를 분석하여 피사체를 자동으로 추출합니다.
*   **✨ 매직 포인트 (Magic Point)**: 원하는 물체를 클릭하면 해당 개체만 똑똑하게 선택하여 남깁니다.
*   **🪄 컬러 지우개 (Color Eraser)**: 특정 색상을 클릭하면 유사한 색상의 배경을 한 번에 날려버립니다.
*   **🖌️ 스마트 브러쉬 (Smart Brush)**: 지우기/복원 모드를 지원하며, 클릭 지점의 색상을 분석하여 주변을 정밀하게 다듬습니다.

### 3. 설정 및 내보내기
*   **매팅 반경 & 감도**: AI 연산 시 테두리를 얼마나 부드럽거나 정밀하게 처리할지 조절합니다.
*   **배경 옵션**: 투명 배경뿐만 아니라 흰색, 검은색, 또는 사용자 지정 색상 배경을 미리 적용할 수 있습니다.
*   **내보내기**: 최종 결과물을 무손실 PNG 파일로 저장합니다.

---

## 💻 실행 방법

본 프로젝트는 별도의 빌드 과정이 필요 없는 정적 웹 애플리케이션입니다.

1.  프로젝트 루트 폴더에서 로컬 서버를 실행합니다.
    ```bash
    npx -y serve . -l 8014
    ```
2.  브라우저에서 `localhost:8014`(또는 출력된 주소)으로 접속합니다.
3.  고화질 이미지 파일을 드래그 앤 드롭하여 매팅 작업을 시작하세요.

---
**Note**: 본 도구는 모든 AI 연산을 사용자의 로컬 GPU/CPU에서 수행하므로 데이터 보안에 안전하며, 높은 사양의 그래픽 환경에서 더 쾌적하게 작동합니다.

---

## 📜 License & Open Source Notice

### Project License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

### Open Source Acknowledgments
This project utilizes the following open source libraries:

*   **Google MediaPipe Tasks Vision**
    *   License: Apache License 2.0
    *   Copyright 2023 Google LLC. All rights reserved.
    *   [https://developers.google.com/mediapipe](https://developers.google.com/mediapipe)
