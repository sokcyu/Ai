# PoseCraft Local

안드로이드 기기 안에서 이미지를 생성·편집하고 사진으로 짧은 MP4를 만드는 앱입니다. 계정, 리워드, 생성 횟수 제한, 유료 API를 사용하지 않습니다.

## 현재 기능

- 문장으로 이미지 생성: MediaPipe Image Generator + 로컬 Stable Diffusion 모델
- 사진 불러오기, 구도 회전, 색감 조절, PNG 저장
- 사진에 줌·이동 효과를 넣은 4초 MP4 생성
- 모델을 기기 저장소에서 한 번 선택해 앱 전용 공간에 복사
- 네트워크 권한 없음

## 설치

1. Android Studio에서 이 폴더를 엽니다.
2. Android SDK 35를 설치하고 휴대폰(Android 12 이상)을 연결합니다.
3. `Run`으로 앱을 설치합니다.
4. Stable Diffusion 1.5 EMA-only 체크포인트를 Google MediaPipe 형식으로 변환한 `bins` 폴더를 휴대폰에 복사합니다.
5. 앱의 **AI 모델 선택**에서 그 폴더를 선택합니다.

모델 변환은 Google의 공식 Image Generator Android 안내를 따르세요:
https://developers.google.com/edge/mediapipe/solutions/vision/image_generator/android

## 현실적인 제한

- MediaPipe Image Generator는 실험적 기능이며 현재 적극적으로 유지보수되지 않습니다.
- 모델은 수 GB가 될 수 있으며 APK에 포함하지 않습니다.
- 로컬 생성 속도는 휴대폰 GPU/OpenCL 지원에 따라 수 분 이상 걸리거나 실행되지 않을 수 있습니다.
- 현재의 “자세 변경”은 구도 회전 편집입니다. 사람의 팔·다리 관절을 새 포즈로 재생성하려면 별도의 포즈 조건 모델과 고성능 GPU가 필요합니다.
- “영상 만들기”는 생성형 비디오가 아니라 사진 기반 Ken Burns 애니메이션입니다.

## 개인정보

사진과 프롬프트는 앱 밖으로 전송되지 않습니다. 저장을 누른 결과만 갤러리에 기록됩니다.
