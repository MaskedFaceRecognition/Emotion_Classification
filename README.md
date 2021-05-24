# Emotion Classification Model Summary
	0429 update : 각 모델 재구축 및 결과 정리 & confusion matrix 수정 & object detection 논문 searching
	0430 update : 0_1 model 재구축 및 confusion matrix 확인완료
		      0_2 Overfitting 해결 ( train과 test 모두 shuffle=True로 지정 ) & confusion matrix 해결( random number로 data set array index 지정 )
	0501 update : 1_1 model 재구축 및 condusion matrix 확인완료
	0512 update : 1_2 model epoch=6에서 local pc 내 디스크 공간 부족 발생 => 로컬 디스크 공간 확보
	0515 update : 1_2 model epoch=19에서 local pc 내 디스크 공강 부족 발생 => colab 이용
	0516 update : 0_3 model 구축 완료
		      1_2 model in colab is stopped at epochs = 23 /60
		      0_4 model 구축 완료
	0517 update : 0_5 model 구축 완료
	0518 update : 1_2 model  " the upper toolbar > select 'Runtime' > 'Change Runtime Type' > hardware accelerator: select 'TPU' " 사용하여 RAM 공간 25GB에서 35.5GB로 확장 후 다시 시도
	0519 update : 1_2 model 구축 완료 ( failed to upload model_best_1_2.h5 cuz of the size )
	              1_2 model confusion matrix 해결
   	0522 update : 2_1 model 구축 완료
		      1_3 model 진행중
	0524 update : 1_3 model in colab ==> run time error
		      2_2 model 진행중
		      

## 0 : Training CNN model => Mini Xception

#### 0_1 : 수정되지 않은 데이터 ( anger, disgust, fear, happiness, sadness, surprise, neutral ) 사용, batch_size = 32, 정확도 52.06%, epochs = 10 
	==> best model model_best_0_1.h5 정확도 0??

#### 0_2 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 82.36%

#### 0_3 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 16 epochs = 60, 정확도 83.25%

#### 0_4 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 8, epochs = 60, 정확도 84.84%

#### 0_5 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 32, epochs = 60, 정확도 82.39%




## 1 : Training CNN model => fernet.png

#### 1_1 : 수정되지 않은 데이터 ( anger, disgust, fear, happiness, sadness, surprise, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 66.53%

#### 1_2 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 91.33(첫 시도는 구축 성공 but, 모델 저장 파일 존재X)
	==> 메모리 부족 문제로 구축 실패

#### 1_2_colab : 1_2와 동일 정확도 84.35%
	==> memory 부족 실패 at epochs =  23
	==> memory 부족 문제 TPU 사용으로 해결
	==> exist model_best_1_2.h5 at https://drive.google.com/file/d/10jv6YsbH2OccjC6xioJ3ID33R5Gsiy1I/view?usp=sharing
	==> exist models_1_2_colab at https://drive.google.com/drive/folders/1ud1Xo5oV8bK3pGo2L9Z6xn4H5ANE5s9g?usp=sharing

#### 1_3 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 8, epochs = 60, train accuracy = 90.98%
	==> confusion matrix 확인 필요



## 2 : Training CNN model => DCNN

#### 2_1 : 수정되지 않은 데이터 ( anger, happiness, sadness, neutral ) 사용, batch_size = 32, epochs = 100, 정확도 78%
	==> exist model_best_2_1.h5 at https://drive.google.com/file/d/1-Fjw4UmNYQYcDs9K-Jt72LsSVquSWrgN/view?usp=sharing

#### 2_2 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 ----
