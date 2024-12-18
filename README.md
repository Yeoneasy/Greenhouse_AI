## 스마트 온실 환경 데이터 인공지능 예측 및 시각화 기술 개발

스마트 온실 환경 데이터 인공지능 예측 및 시각화 기술 개발을 목표로 하는 프로젝트입니다. 
이 프로젝트의 목표는 머신러닝 모델을 활용하여 작물 성장에 최적의 조건을 유지하는 수치를 찾아 자동화를 목표로 합니다.

### 주요 기능
- **데이터 분석**: 온실 센서의 시계열 데이터를 분석.
- **인공지능 예측**: LSTM 및 강화 학습을 사용하여 내부 온도와 제어 값을 예측.
- **제어 최적화**: AI 예측을 기반으로 구동기를 동적으로 조정.

### 데이터 설명
이 프로젝트는 실제 온실 데이터를 활용합니다. 주요 데이터는 다음과 같습니다:
- **외부 데이터**: 온도, 풍향, 풍속, 일사량, 강우량 등.
- **내부 데이터**: 온도, 습도.
- **제어 데이터**: 난방 및 환기 설정값.
- **구동기 데이터**: 창문, 커튼, 밸브 위치의 개도율.

### 모델 학습
LSTM 모델 학습:
```bash
python train_lstm.py
```

구동기 제어값 학습:
```bash
python train_rl.py
```

### 디렉토리 구조
```
SmartGreenhouseAI/
├── data/
│   ├── raw/               # 원본 온실 데이터셋
│   ├── processed/         # 전처리된 데이터셋
├── models/                # 학습된 모델 파일
├── notebooks/             # 분석용 Jupyter 노트북
├── src/                   # 소스 코드
│   ├── data_processing/   # 데이터 전처리 스크립트
│   ├── models/            # 모델 아키텍처
│   ├── rl/                # 강화 학습 모듈
├── requirements.txt       # 필요한 Python 패키지
├── train_lstm.py          # LSTM 모델 학습 스크립트
├── train_rl.py            # 강화 학습 모델 학습 스크립트
├── visualize.py           # 데이터 시각화 스크립트
```

### 요구 사항
- Python 3.8+
- TensorFlow 또는 PyTorch
- Matplotlib
- Pandas
- NumPy
