## 1주차. 딥러닝 Basic

### Deep Learning의 요소들

1. Data : 다루는 Task가 무엇인지에 따라서 다양함
2. Model : 우리에게 주어진 data가 input으로 들어간 경우, 우리가 원하는 output으로 만들어주는 프로그램
3. Loss function : 다루는 Task가 무엇인지에 따라서 다름
   - 학습 중 알고리즘이 잘못 예측한 정도에 대한 지표를 의미
4. Optimization and Regularization
   - Optimization : 정답 값에 빠르고 정확하게 다다르기 위해서 'Gradient Descent Method(경사하강법)'을 사용
   - Regularization : 학습을 방해하며 일반화 성능을 높임

### Neural Network

: 인간의 지능을 모방하니까, 인간의 뉴런과 비슷한 모습으로 네트워크를 구상한 것
BUT 요즘 사용되는 것은 뉴런 이미지와는 다른 양상을 보임 - matrix multiplication & nonlinear function을 사용

1. Nonlinear Function : 비선형 함수
   - 모델의 표현력을 극대화시키기 위해서 (우리가 원하는 output을 빠르게 얻기 위해서)
2. Multi-Layer Perceptron : 뉴런 네트워크를 이루고 있는 Perceptron들이 여러 겹으로 쌓여있는 것

### Generalization

: 일반화 성능을 높이기 위해서 필요한 방법들은 다음과 같다

1. Cross Validation (교차검증)
2. Ensemble : 여러개의 분류 모델을 조합하여 성능 향상
   - Bagging : 각각의 예측 결과를 평균 내거나 투표하는 방법을 사용
   - Boosting : 학습 제대로 X된 데이터들을 모아서, 새로운 모델로 순차적으로 학습시킴 (강한 예측 모델 생성 가능)
3. Regularization : 학습을 방해하는 방법
   - Parameter norm penalty : 뉴런 네트워크의 paramater가 너무 커지지 X도록 하는 것
   - Noise Robustness : 엉뚱한 데이터가 들어와도 흔들리지 X게 만들기 위해서
   - Label smoothing : 모델의 일반화 능력을 향상시켜주는 기술
