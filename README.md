# Emotion Classification Model Summary
	0429 update : 각 모델 재구축 및 결과 정리 & confusion matrix 수정 & object detection 논문 searching
	0430 update : 0_1 model 재구축 및 confusion matrix 확인완료
		      0_2 Overfitting 해결 ( train과 test 모두 shuffle=True로 지정 ) & confusion matrix 해결( random number로 data set array index 지정 )

## 0 : Training CNN model => Mini Xception

#### 0_1 : 수정되지 않은 데이터 ( angry, disgust, fear, happy, sad, surprise, neutral ) 사용, batch_size = 32, 정확도 52.06%, epochs = 10 
	==> best model model_best_0_1.h5 정확도 0??
	==> confusion matrix 확인 필요


#### 0_2 : 수정된 데이터 ( angry, happy, neutral ) 사용, batch_size = 64, shuffle=True, epochs = 60, 정확도 84.29%

#### 0_2(1) : 수정된 데이터 ( angry, happy, neutral ) 사용, batch_size = 64, 자체 shuffle 진행, epochs = 10, 정확도 --?--
	==> Overflow!!!!
	==> confusion matrix 확인 필요



## 1 : Training CNN model => fernet.png

#### 1_1 : 수정되지 않은 데이터 ( angry, disgust, fear, happy, sad, surprise, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 --?--
	==> confusion matrix 확인 필요

#### 1_2 : 수정된 데이터 ( angry, happy, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 91.33
	==> 결과 재확인 필요
	==> confusion matrix 확인 필요

#### 1_2(1) : 수정된 데이터 ( angry, happy, neutral ) 사용, batch_size = 64, test shuffle = True, epochs = 60, 정확도 --?--
	==> 결과 확인 필요
	==> overfitting 여부 & confusion matirx 정확도 확인 필요


#### 1_3 : 수정된 데이터 (angry, happy, neutral ) 사용, batch_size = 8, test shuffle = True, epochs = 60, train accuracy = 90.98%
	==> confusion matrix 확인 필요
