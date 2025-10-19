# MLP vs CNN

이 폴더는 **Fashion MNIST** 이미지 데이터셋을 기반으로,  
다층 퍼셉트론(MLP)과 합성곱 신경망(CNN)의 **성능과 구조적 차이**를 비교·분석하는 실습을 포함하고 있습니다.  

MLP는 여러 개의 퍼셉트론 뉴런을 깊게 쌓은 구조이지만,  
층이 깊어질수록 **학습이 어려워지는 한계**(**vanishing gradient**)가 존재합니다.  
반면 CNN은 여러 은닉층에서 **계층적인 특징**(**Feature hierarchy**)을 자동으로 추출하여,  
**이미지·영상 처리에 뛰어난 성능**을 보입니다.  

본 실습에서는 두 모델을 동일한 Fashion MNIST 데이터에 적용하여,  
훈련 결과(정확도, 손실 변화, 시각화 결과 등)를 비교하고  
**딥러닝 구조에 따른 학습 효율 차이**를 직접 확인할 수 있습니다.

# 주요 내용

- **MLP 모델**을 이용한 학습 및 시각화 실습
- **CNN 모델**을 이용한 학습 및 시각화 실습
- 두 모델의 성능 비교 및 결과 해석

## 파일 구성
- `01_data_load.ipynb`: Fashion MNIST 데이터셋 시각화
- `02_MLP_train.ipynb`: MLP 모델 학습 실습
- `03_CNN_train.ipynb`: CNN 모델 학습 실습
- `data_loader.py`: 데이터 로딩 및 전처리 모듈
- `CNN_train_result.png`: CNN 테스트 결과 시각화 이미지
- `MLP_train_result.png`: MLP 테스트 결과 시각화 이미지
- `notes.md`: 실험 정리 및 메모
- `data`: 데이터 저장 디렉토리

## 실험 결과 요약

## 📈 실험 결과 요약

| 모델 | 테스트 정확도(%) | 학습 시간 | 특징 |
|:-----|:----------------:|:-----------:|:------|
| **MLP** | 83.51 | 빠름 | 단순 구조, 이미지 특성 반영 한계 |
| **CNN** | 92.14 | 보통 | 공간적 패턴 학습, 시각 데이터에 강점 |

> CNN이 이미지 내 공간 구조를 반영하기 때문에, MLP보다 높은 정확도를 보임.

<p align="center">
  <img src="D:/project/MLPvsCNN/CNN_train_result.png" width="600"><br>
  <em>CNN 훈련 손실 및 정확도</em>
</p>

<p align="center">
  <img src="D:/project/MLPvsCNN/mlp_train_result.png" width="600"><br>
  <em>MLP 훈련 손실 및 정확도</em>
</p>

