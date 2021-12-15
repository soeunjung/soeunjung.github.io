# numpy

### ndarray


```python
import numpy as np
```


```python
array1=np.array([1,2,3])
print(type(array1))
print(array1.shape)  #1차원

array2=np.array([[1,2,3],[2,3,4]])
print(type(array2))
print(array2.shape)  #2차원

array3=np.array([[1,2,3]])
print(type(array3))
print(array3.shape)  #1row, 2col로 이루어진 2차원
```

    <class 'numpy.ndarray'>
    (3,)
    <class 'numpy.ndarray'>
    (2, 3)
    <class 'numpy.ndarray'>
    (1, 3)
    

### ndarray datatype

ndarray 내의 datatype은 그 연산의 특성 상 같은 datatype만 존재 가능


```python
list1=[1,2,3]
print(type(list1))
array1=np.array(list1)  #list to array
print(type(array1))
print(array1,array1.dtype)
```

    <class 'list'>
    <class 'numpy.ndarray'>
    [1 2 3] int32
    

다른 datatype이 섞여있으면 크기가 더 큰 datatype으로 형 변환을 일괄 적용


```python
list2=[1,2,'test']
array2=np.array(list2)
print(array2,array2.dtype)  #int to unicode

list3=[1,2,3.0]
array3=np.array(list3)
print(array3,array3.dtype)  #int to float
```

    ['1' '2' 'test'] <U11
    [1. 2. 3.] float64
    

astype() :: datatype을 쉽게 변경


```python
array_int=np.array([1,2,3])
array_float=array_int.astype('float64')
print(array_float,array_float.dtype)

array_int1=array_float.astype('int32')
print(array_int1,array_int1.dtype)

array_float1=np.array([1.1,1.2,3.1])
array_int2=array_float1.astype('int32')
print(array_int1,array_int1.dtype)

```

    [1. 2. 3.] float64
    [1 2 3] int32
    [1 2 3] int32
    

arange()


```python
sequence_array=np.arange(10)
print(sequence_array)
print(sequence_array.dtype,sequence_array.shape)
```

    [0 1 2 3 4 5 6 7 8 9]
    int32 (10,)
    

zeros()


```python
zero_array=np.zeros((3,2),dtype='int32')
print(zero_array)
print(zero_array.dtype,zero_array.shape)
```

    [[0 0]
     [0 0]
     [0 0]]
    int32 (3, 2)
    

reshape()


```python
array1=np.arange(10)
print(array1)
array2=array1.reshape(2,5)
print(array2)
array3=array1.reshape(5,2)
print(array3)
```

    [0 1 2 3 4 5 6 7 8 9]
    [[0 1 2 3 4]
     [5 6 7 8 9]]
    [[0 1]
     [2 3]
     [4 5]
     [6 7]
     [8 9]]
    

### Indexing

단일 값 추출


```python
#1부터 9까지의 1차원 ndarray 생성
array1=np.arange(1,10)
print(array1)
value=array1[2]
print(value,type(value))
```

    [1 2 3 4 5 6 7 8 9]
    3 <class 'numpy.int32'>
    

슬라이싱


```python
array1=np.arange(1,10)
array3=array1[0:3]
print(array3,type(array3))
```

    [1 2 3] <class 'numpy.ndarray'>
    

### 선형대수 연산 - 행렬 내적과 전치 행렬 구하기

행렬 내적(행렬 곱)


```python
A=np.array([[1,2,3],[4,5,6]])
B=np.array([[7,8],[9,10],[11,12]])
dot_product=np.dot(A,B)
dot_product
```




    array([[ 58,  64],
           [139, 154]])



전치 행렬


```python
A=np.array([[1,2],[3,4]])
transpose_mat=np.transpose(A)
transpose_mat
```




    array([[1, 3],
           [2, 4]])




```python

```
