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
	0525 update : 2_2 model 구축 완료
		      2_3 model 진행중
		      1_3 model 0327 구축 모델 확인
