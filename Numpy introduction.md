
#Introduction to Numpy #

*Numpy is...*


```python
#Numpy arrays
import numpy as np
```


```python
import numpy as np
```


```python
#create a numpy array
list_1 = [1,2,3,4]
list_1
```




    [1, 2, 3, 4]




```python
np.array(list_1)
```




    array([1, 2, 3, 4])




```python
np.arange(1,10)
```




    array([1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
np.arange(1,10, 2)
```




    array([1, 3, 5, 7, 9])




```python
np.zeros(5)
```




    array([0., 0., 0., 0., 0.])




```python
np.zeros((5,4)) # is a two dimens array -has 2 [[ at the beginning compared to one dimens.arrays [
```




    array([[0., 0., 0., 0.],
           [0., 0., 0., 0.],
           [0., 0., 0., 0.],
           [0., 0., 0., 0.],
           [0., 0., 0., 0.]])




```python
np.ones((4,5))
```




    array([[1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.]])




```python
np.linspace(0, 10,101)
```




    array([ 0. ,  0.1,  0.2,  0.3,  0.4,  0.5,  0.6,  0.7,  0.8,  0.9,  1. ,
            1.1,  1.2,  1.3,  1.4,  1.5,  1.6,  1.7,  1.8,  1.9,  2. ,  2.1,
            2.2,  2.3,  2.4,  2.5,  2.6,  2.7,  2.8,  2.9,  3. ,  3.1,  3.2,
            3.3,  3.4,  3.5,  3.6,  3.7,  3.8,  3.9,  4. ,  4.1,  4.2,  4.3,
            4.4,  4.5,  4.6,  4.7,  4.8,  4.9,  5. ,  5.1,  5.2,  5.3,  5.4,
            5.5,  5.6,  5.7,  5.8,  5.9,  6. ,  6.1,  6.2,  6.3,  6.4,  6.5,
            6.6,  6.7,  6.8,  6.9,  7. ,  7.1,  7.2,  7.3,  7.4,  7.5,  7.6,
            7.7,  7.8,  7.9,  8. ,  8.1,  8.2,  8.3,  8.4,  8.5,  8.6,  8.7,
            8.8,  8.9,  9. ,  9.1,  9.2,  9.3,  9.4,  9.5,  9.6,  9.7,  9.8,
            9.9, 10. ])




```python
np.eye(5)
```




    array([[1., 0., 0., 0., 0.],
           [0., 1., 0., 0., 0.],
           [0., 0., 1., 0., 0.],
           [0., 0., 0., 1., 0.],
           [0., 0., 0., 0., 1.]])




```python
#NUMPY RANDOM MODULES (to insert np.random.+ tab to see the options)
np.random.rand(3)
```




    array([0.01838286, 0.11753786, 0.61630369])




```python
np.random.rand(3,4) # returns 2dimens.array with 3 rows and 4 columns
```




    array([[0.10309098, 0.21506996, 0.64513432, 0.07299564],
           [0.86508434, 0.73611755, 0.8950842 , 0.28588474],
           [0.15390598, 0.54270006, 0.46729401, 0.79228669]])




```python
#Randn
np.random.randn(5)
```




    array([-0.22332825,  0.02688538,  0.53752656,  1.58970832,  0.64240714])




```python
np.random.randn(3,5)
```




    array([[-0.93187865, -0.08139741, -1.7248639 ,  0.20589224, -1.05766024],
           [ 0.46103992,  0.42343776,  0.97668888, -0.7143784 ,  0.37547701],
           [ 0.75284647, -0.03228995,  0.27664745, -0.20410682, -0.29215571]])




```python
np.random.randint(10,20)
```




    19




```python
arr = np.arange(1,20, 2)
arr
```




    array([ 1,  3,  5,  7,  9, 11, 13, 15, 17, 19])




```python
arr.reshape(10,1)

```




    array([[ 1],
           [ 3],
           [ 5],
           [ 7],
           [ 9],
           [11],
           [13],
           [15],
           [17],
           [19]])




```python
arr.max()
```




    19




```python
arr.min()
```




    1




```python
arr.argmax()
```




    9




```python
arr.argmin()
```




    0



# Numpy Operations #


```python
arr2 = np.arange(1,10)
arr3 = np.arange(11,20)
```


```python
arr2
```




    array([1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
arr3
```




    array([11, 12, 13, 14, 15, 16, 17, 18, 19])




```python
arr2 + arr3
```




    array([12, 14, 16, 18, 20, 22, 24, 26, 28])




```python
arr2 * arr3
```




    array([ 11,  24,  39,  56,  75,  96, 119, 144, 171])




```python
arr2 ** arr3
```




    array([                  1,                4096,             1594323,
                     268435456,         30517578125,       2821109907456,
               232630513987207,   18014398509481984, 1350851717672992089])




```python
arr2 *4
```




    array([ 4,  8, 12, 16, 20, 24, 28, 32, 36])



### Numpy Indexing and Selection ###


```python
example_arr = np.arange(1,21).reshape(4,5)
```


```python
example_arr
```




    array([[ 1,  2,  3,  4,  5],
           [ 6,  7,  8,  9, 10],
           [11, 12, 13, 14, 15],
           [16, 17, 18, 19, 20]])




```python
example_arr[3]
```




    array([16, 17, 18, 19, 20])




```python
example_arr[:2,:2]
```




    array([[1, 2],
           [6, 7]])




```python
example_arr[:2,2:]
```




    array([[ 3,  4,  5],
           [ 8,  9, 10]])



### Broadcasting ###


```python
example_arr[1:4] = 30
```


```python
example_arr
```




    array([[ 1,  2,  3,  4,  5],
           [30, 30, 30, 30, 30],
           [30, 30, 30, 30, 30],
           [30, 30, 30, 30, 30]])



example_arr[3] = [10,20,30,40,50]


```python
example_arr
```




    array([[ 1,  2,  3,  4,  5],
           [30, 30, 30, 30, 30],
           [30, 30, 30, 30, 30],
           [10, 20, 30, 40, 50]])



### Conditional selection ###


```python
example_arr2 = np.arange(21,41).reshape(4,5)
```


```python
example_arr2 
```




    array([[21, 22, 23, 24, 25],
           [26, 27, 28, 29, 30],
           [31, 32, 33, 34, 35],
           [36, 37, 38, 39, 40]])




```python
example_arr2 >30
```




    array([[False, False, False, False, False],
           [False, False, False, False, False],
           [ True,  True,  True,  True,  True],
           [ True,  True,  True,  True,  True]])




```python
example_arr2[example_arr2 >30]
```




    array([31, 32, 33, 34, 35, 36, 37, 38, 39, 40])




```python
example_arr2[(example_arr2 >30) & (example_arr2 <35)]
```




    array([31, 32, 33, 34])




```python

```
