# 데이터 핸들링을 위한 라이브러리 NumPy

## NumPy
- Numerical Python
  - 파이썬에서 대규모 다차원 배열을 다루는 라이브러리
  - 반복문 없이 배열 처리 가능
  - 파이썬 리스트에 비해, 빠른 연산을 지원하고 메모ㄹ를 효율적으로 사용
  - 리스트의 요소는 콤마(,)로 구분한다
  - 여러 타입의 데이터를 복합적으로 저장할 수 있음
  ``` python
    list_arr = list(range(5))
    print(list_arr)         # [0,1,2,3,4] -> 콤마(,)로 구분 
    print(type(list_arr))   # <class 'list'>
  ```
  
- NumPy 사용
``` Python
  import Numpy as np
  # numpy 모듈을 불러와서 'np' 별칭 부여
```
- 배열 생성하기
``` Python
  import NumPy as np
  np_arr = np_array(range{5))
  print(np_arr)           # [0 1 2 3 4] -> 공백으로 구분
  print(type(np_arr))     # <class 'numpy.ndarray'>
```
- 배열의 데이터 타입 : dtype
  - 같은 데이터 타입만 저장 할 수 있다
  ``` Python
    arr = np.array([0,1,2,3,4], dtype=float)
    print(arr)              # [0. 1. 2. 3. 4.]
    print(arr.dtype)        # float64
    print(arr.astype(int))  # [0 1 2 3 4]
  ```
- 배열의 속성
  - ndim : 배열의 차원
  - shape : 차원의 형태
   ``` Python
    print(arr.dim)
    print(arr.shape)
    # arr.dim이 1 이면, arr.shpae sms ((데이터 개수), )로 표현
    
    arr.shape = n,m
    print("arr.shpae : {}".format(arr.shpae))     # arr.shape = (n.m)
    print("배열의 요소의 수 : {}".format(arr.size))   # 배열 요소의 수 : n * m
    print("배열의 길이 : {}".format(len(arr)))       # 배열의 길이 : n
   ```
   
- indexing과 slicing
  - indexing : 인덱스로 값을 찾아냄
  ``` Python
    x = np.arange(7)
    print(x)    # [0 1 2 3 4 5 6]
    print(x[3]) # 3
    print(x[7]) # IndexError: index 7 is out of bounds
    x[0] = 10
    print(x)    # [10 1 2 3 4 5 6]
  ```
  ```python
    x = np.aragne(1, 13, 1)
    x.shape = 3,4
    print(x)
    # [[1 2 3 4]
       [5 6 7 8]
       [9 10 11 12]]
    print(x[2,3]) # 12
  ```
  - slicing: 인덱스 값으로 배열의 일부분을 가져옴
  ``` Python
    x = np.arange(7)
    print(x) #[0 1 2 3 4 5 6]
    
    # x[start:end]
    # start 이상 end 미만 인덱스의 값을 배열형태로 추출
  ```

  - Boolean indexing : 배열의 각 요소의 선택 여부를 Boolean mask를 이용하여 지정하는 방식
  ```Python
    x = np.arange(7)
    
    print(x)          # [0 1 2 3 4 5 6]
    print(x < 3)      # [True True True False False False False]
    print(x > 7)      # [False False False False False False False]
    print(x[x<3])     # [0 1 2]
    print(x[x%2 == 0] # [0 2 4 6]
  ```
  
  - Fancy indexing : 배열의 각 요소 선택을 index 배열을 전달하여 지정하는 방식
  ``` Python
    x = np.arange(7)
    print(x[[1,3,5]]  #[1 3 5]
    x = np.arange(1,13,1).reshape(3,4)
    print(x)
    # [[1 2 3 4]
       [5 6 7 8]
       [9 10 11 12]]
    print(x[[0, 2]])
    # [[1 2 3 4]
       [9 10 11 12]]
  ```
  
  
  
  
  
