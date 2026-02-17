# Emotion Mirror

실시간 표정 감정 분석 웹 앱 — 온디바이스 AI

🔗 **[Live Demo](https://geeksbaek.github.io/emotion-mirror/)**

## 소개

웹캠을 통해 실시간으로 얼굴을 감지하고 7가지 감정(행복, 슬픔, 분노, 놀람, 혐오, 공포, 중립)을 분석합니다. 모든 추론이 브라우저 내에서 수행되므로, 서버로 영상 데이터가 전송되지 않습니다.

## 주요 기능

- **실시간 얼굴 감지** — TinyFaceDetector + 68-point 랜드마크
- **감정 인식** — OpenCV Progressive Teacher 모델 (ONNX Runtime)
- **시각화** — 감정 분포 바 차트 + 시간별 타임라인 차트
- **실시간 파비콘** — 감지된 감정에 따라 브라우저 탭 아이콘이 이모지로 변경
- **반응형 디자인** — 모바일, 태블릿, 데스크톱, 가로 모드 모두 지원
- **온디바이스 추론** — 개인정보 보호, 서버 전송 없음
- **백그라운드 모드** — 탭 비활성 시 자동으로 추론 간격 조절

## 기술 스택

| 역할 | 기술 |
|---|---|
| 얼굴 감지/랜드마크 | [face-api.js](https://github.com/vladmandic/face-api) (TF.js) |
| 감정 인식 | [OpenCV FER MobileFaceNet](https://huggingface.co/opencv/facial_expression_recognition) (ONNX Runtime) |
| 차트 | [Chart.js](https://www.chartjs.org/) |
| 추론 백엔드 | 데스크톱: WebGPU / 모바일: WebGL + WASM |

## 요구 사항

- **브라우저**: Chrome, Edge, Safari 등 최신 브라우저
- **웹캠**: 카메라 접근 권한 필요

## 실행

별도 빌드 없이 `index.html`을 열면 됩니다. 모든 의존성은 CDN에서 로드됩니다.

로컬 서버로 실행하려면:

```bash
npx serve .
```

## 라이선스

MIT
