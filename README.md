# Emotion Classification Model Summary

	* All models used fer2013 data as sample data
	* You can see all checkpoints of each models at https://drive.google.com/drive/folders/1hskIQnNTQOURUH5a-f45LPSXG0Oi_vdp?usp=sharing

## 0 : Training CNN model => Mini Xception

#### 0_1 : 수정되지 않은 데이터 ( anger, disgust, fear, happiness, sadness, surprise, neutral ) 사용, batch_size = 32, 정확도 52.06%, epochs = 10 

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

#### 1_3 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 8, epochs = 60, train accuracy = 84.79%



## 2 : Training CNN model => DCNN

#### 2_1 : 수정되지 않은 데이터 ( anger, happiness, sadness, neutral ) 사용, batch_size = 32, epochs = 100, 정확도 78%
	==> exist model_best_2_1.h5 at https://drive.google.com/file/d/1-Fjw4UmNYQYcDs9K-Jt72LsSVquSWrgN/view?usp=sharing

#### 2_2 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 64, epochs = 60, 정확도 84.46%
	==> exist model_best_2_2.h5 at https://drive.google.com/file/d/17I53Ks3UVeW5y_N5y3ln1wTn4dAZSdDZ/view?usp=sharing

#### 2_3 : 수정된 데이터 ( anger, happiness, neutral ) 사용, batch_size = 64, epochs = 120, 정확도 ---


