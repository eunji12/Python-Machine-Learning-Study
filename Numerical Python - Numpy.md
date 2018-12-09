### Numerical Python - Numpy
```
2018-12-06  python numpy ~ shape handling
2018-12-09  slicing ~ fancy index
* 간단한 정리, edwidt 2_3_Numpy.pdf 파일에 자세한 내용 있음
```

python 특징
dynamic typing
실행시점에 데이터 타입 지정 
하나의 리스트에도 다양한 타입 가능 

numpy는 허용X
 np.array(["1","4",5,8],float)
로 지정하면 문자나 숫자로 타입으로 출력 되지않고
array([1., 4., 5., 8.]) float형으로 출력(지정한 타입으로)
>> 하나의 데이터타입만 배열에 넣을 수 있음
>> np.array와 python list의 차이

* np.array => ndarray
* 넘파이는 하나의 데이터 타입만 배열에 넣을 수 있다
* 리스트와 가장 큰 차이점이다
* C의 array를 사용하여 배열 생성

ndim
size

[shape handling)
- reshape : array의 shape의 크기를 변경함
- 데이터를 호출하게 되면 y 값이 보통 vector로 들어오는데
사이킷 런을 쓰려면 matrix 값으로 넣어줘야함
- 머신러닝에선 그래서 reshape을 사용함
- np.array(test_matrix).reshape(-1,2)
* -1: None, none 와 같은, size를 기반으로 row개수 선정
 > row수를 정하지 못했을때 -1 값을 주면 size에 따라 지정

*tuple 다시 알기

* flatten() 다차원배열을 1차원으로 바꿔줌
- reshape 을 사용해도 되지만 flatten써주면 더 쉽게 펴짐
>>> test_array
array([[1., 2., 3., 4.],
       [5., 6., 7., 8.]])
>>> test_array = test_array.flatten()
>>> test_array
array([1., 2., 3., 4., 5., 6., 7., 8.])


[indexing & slicing] 
- indexing
배열 호출 시 a[0][0] 형태와 a(0,0) 두 형태 모두 지원, 
- slicing
a(:,::2) 인 경우 전체 행의 전체열을 2스텝으로
- np.zeros, np.ones, np.empty 로 행열 생성
- np.eye(N=3, M=5, dtype=np.int) 대각이 1인 행열 생성
-  np.digo(matrix) 대각 행렬의 값 추출
- ramdom sampling 가능

[numpy broadcasting]
- shape이 다른 배열간 연산 지원(매트릭스, 스칼라 등)
ex) 
a = np.array([[1,2,3],[4,5,6]])
b = np.array([3])
a+b
array([[4, 5, 6],
       [7, 8, 9]])
- comparisons broadcasting
 >>> c
array([[4, 5, 6],
       [7, 8, 9]])
c >6
array([[False, False, False],
       [ True,  True,  True]])
- argmax, argmin 최대, 최소값의 인덱스 반환
- where ;index
[fancy index]
- array를 인덱스 값을 사용하여 추출하는 방법
 a = np.array([1,2,3,4])
 b = np.array([0,3,2,1],int)
a[b]
array([1, 4, 3, 2])
a = np.array([1,2,3,4],float)
a[b]
array([1., 4., 3., 2.])
a.take(b)
array([1., 4., 3., 2.])

for문이 제일 느리다.

기타 실습 소스
```

-----------------------------------------------
Python 3.6.7 (v3.6.7:6ec5cf24b7, Oct 20 2018, 13:35:33) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.
>>> import numpy as np
>>> test_array = np.array(["1","4",5,8],float)
>>> test_array
array([1., 4., 5., 8.])
>>> print(test_array)
[1. 4. 5. 8.]
>>> type(test_array)
<class 'numpy.ndarray'>
>>> type(test_array[3])
<class 'numpy.float64'>
>>> test_array.dtype
dtype('float64')
>>> test_array.shape
(4,)
>>> test_array
array([1., 4., 5., 8.])
>>> test_array = np.array([[1,2,3,4],[5,6,7,8]],float)
>>> test_array
array([[1., 2., 3., 4.],
       [5., 6., 7., 8.]])
>>> test_array.shape
(2, 4)
>>> test_array.size
8
>>> test_array.ndim
2
>>> test_array.reshape(-1,2)
array([[1., 2.],
       [3., 4.],
       [5., 6.],
       [7., 8.]])
>>> test_array.shape
(2, 4)
>>> test_array
array([[1., 2., 3., 4.],
       [5., 6., 7., 8.]])
>>> np.array(test_array).reshape(-1,2)
array([[1., 2.],
       [3., 4.],
       [5., 6.],
       [7., 8.]])
>>> test_array
array([[1., 2., 3., 4.],
       [5., 6., 7., 8.]])
>>> test_array = test_array.reshape(-1,2)
>>> test_array
array([[1., 2.],
       [3., 4.],
       [5., 6.],
       [7., 8.]])
>>> test_array.shape
(4, 2)
>>> test_array.size
8
>>>  test_array.ndim
SyntaxError: unexpected indent
>>> test_array.ndim
2
>>> test_array
array([[1., 2.],
       [3., 4.],
       [5., 6.],
       [7., 8.]])
>>> test_array = test_array.flatten
>>> test_array
<built-in method flatten of numpy.ndarray object at 0x0000000002CB3D00>
>>> print(test_array)
<built-in method flatten of numpy.ndarray object at 0x0000000002CB3D00>
>>> test_array = np.array([[1,2,3,4],[5,6,7,8]],float)
>>> test_array
array([[1., 2., 3., 4.],
       [5., 6., 7., 8.]])
>>> test_array = test_array.flatten()
>>> test_array
array([1., 2., 3., 4., 5., 6., 7., 8.])
>>> 
```

















