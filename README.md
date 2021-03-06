## 목차
1. [세미나 개요](https://github.com/eunji12/Python-Machine-Learning-Study)
2. [딥러닝이란 무엇인가?](https://github.com/eunji12/Python-Machine-Learning-Study/blob/master/1.%EB%94%A5%EB%9F%AC%EB%8B%9D%EC%9D%B4%EB%9E%80%20%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%3F.md)   
3. [MAC OS에 MINICONDA, JUPYTER NOTEBOOK 설치하기](https://github.com/eunji12/Python-Machine-Learning-Study/blob/master/2%20MAC%20OS%EC%97%90%20MINICONDA%2C%20JUPYTER%20NOTEBOOK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0%20%20.md)
4. [신경망의 수학적 구성 요소_MNIST구현](https://github.com/eunji12/Python-Machine-Learning-Study/blob/master/3.%20%EC%8B%A0%EA%B2%BD%EB%A7%9D%EC%9D%98%20%EC%88%98%ED%95%99%EC%A0%81%20%EA%B5%AC%EC%84%B1%EC%9A%94%EC%86%8C%20-1.md)
5. python 문법과 numpy학습    
6. [Numpy(Numerical Python)](https://github.com/eunji12/Python-Machine-Learning-Study/blob/master/5.%20Numerical%20Python%20-%20Numpy.md)  
7. ▼ tensorflow 실습자료 (유튜브 김성훈 교수 강의) 
 - [ML_lab_01_TensorFlow의_설치_및_기본적인_오퍼레이션](https://colab.research.google.com/github/eunji12/Python-Machine-Learning-Study/blob/master/.ipynb_checkpoints/ML_lab_01_TensorFlow%EC%9D%98_%EC%84%A4%EC%B9%98_%EB%B0%8F_%EA%B8%B0%EB%B3%B8%EC%A0%81%EC%9D%B8_%EC%98%A4%ED%8D%BC%EB%A0%88%EC%9D%B4%EC%85%98-checkpoint.ipynb)  
 - [ML_lec_02_Linear_Regression의_Hypothesis_와_cost_설명](https://colab.research.google.com/github/eunji12/Python-Machine-Learning-Study/blob/master/ML_lec_02_Linear_Regression%EC%9D%98_Hypothesis_%EC%99%80_cost_%EC%84%A4%EB%AA%85.ipynb)  
 - [lab03 cost 확인하기 1.ipynb](https://colab.research.google.com/github/eunji12/Python-Machine-Learning-Study/blob/master/lab03%20cost%20%ED%99%95%EC%9D%B8%ED%95%98%EA%B8%B0%201.ipynb)
 - [lab03 cost 확인하기 2.ipynb](https://colab.research.google.com/github/eunji12/Python-Machine-Learning-Study/blob/master/lab03%20cost%20%ED%99%95%EC%9D%B8%ED%95%98%EA%B8%B0%202.ipynb)

----------------------------
2018-10-08 ~ 2018-12-31
## 주제
python & machine learning (tensorflow) 학습을 통한 MNIST 구현

## 주제 선택 이유
파이썬의 다양한 장점과 신기술 접목, 재미

##### * 파이썬의 다양한 장점
- 쉽고 강력, 높은 생산성, 다양한 라이브러리
- 웹서비스(Django), 데이터분석(Pandas), 머신러닝(Tensorflow)에 강세 

## 예상 산출물
- MNIST 데이터 셋을 이용한 손글씨 인식 구현(tensorflow library)
	- [yann.lecun.com](http://yann.lecun.com/exdb/mnist/) 에서 제공하는 대량의 손글씨 이미지 데이터를 학습하여 새로운 손글씨가 입력될 경우 학습된 데이터를 기반으로 값을 판별하는 프로그램 구현  
	- 머신러닝의 대표적 입문 문제
	- 필기 숫자들의 28x28 픽셀 이미지를 보고, 0부터 9까지의 모든 숫자들에 대해 이미지가 어떤 숫자를 나타내는지 판별하는 것

<img src="https://tensorflowkorea.gitbooks.io/tensorflow-kr/content/g3doc/images/mnist_digits.png"/>  


- python 학습 및 실습 자료 제출(github)
 	- [https://github.com/eunji12/Python-Machine-Learning-Study](https://github.com/eunji12/Python-Machine-Learning-Study)  
	
## 세부 일정

- ~ 2018.10.13 : 세미나 진행 계획 수립
- 1주차(~ 2018.10.21) : 파이썬 설치 및 언어 기초 학습
- 2~3주차(2018.10.22 ~ 2018.11.04) :   
mnist구현에 필요한 이론 학습(tensorflow, 뉴럴네트워크, one-hot, cnn, keras:오픈소스 신경망 라이브러리 등), 실습환경 세팅(jupyter notebook, miniconda,.)
- 4~7주차(2018.11) : MNIST 구현 + 이론 학습 연장
- 8주차(2018.12.03~ ) : 프로젝트 완료 및 산출물 정리 

## 학습 자료
- youtube 김성훈 교수의 [모두를 위한 딥러닝](https://www.youtube.com/playlist?list=PLlMkM4tgfjnLSOjrEJN31gZATbcj_MpUm)
- edwith [머신러닝을 위한 파이썬](https://www.edwith.org/aipython)
- 파이썬 프로그래밍(조인석)
- Hands-On Machine Learning with Scikit-Learn &Tensorflow
- [DJango 시작하기](http://heiswed.tistory.com/entry/%EC%9E%A5%EA%B3%A0-%EA%B0%9C%EB%B0%9C-%ED%99%98%EA%B2%BD-%EC%9D%B4%ED%81%B4%EB%A6%BD%EC%8A%A4-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0?category=616442)
- [keras](https://keras.io/)
- [컨볼루션 신경망](http://aikorea.org/cs231n/convolutional-networks/)
- [점프투파이썬](https://wikidocs.net/30)
- [keras 가이드](https://keras.io/getting-started/sequential-model-guide/)  
## 최종 목표
구현 기술, 머신 러닝에 대한 이론적 이해를 하고 활용 가능한 지식 쌓기




