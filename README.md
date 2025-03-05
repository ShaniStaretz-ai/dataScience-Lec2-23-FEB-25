# dataScience-Lec2-23-FEB-25
start of numpy
* shift+tab for help, when standing on the function
* ?np.array=help
* need import numpy library and use it's functions as np
    ```
        import numpy as np
    ```
* np.array is same as list but **must faster** performance and uses less memory.
* create array:
  * first=np.array([1,2,3])
  * second=np.array([4,5,6],dtype=int) type of elements is int
    * if the element are in float type, it will change to int:
      * array([1.1111,2,3])=[1,2,3]
    * if dtype=float: some elements are in other type, the type will change and leave after the '.'
    same spaces numbers like the other elements
    * example:
    ```
    first_np_arr=np.array([1.11,2.987654,3],dtype=float)
    [1.11     2.987654 3.      ]
    ```
    meaning the spaces added to other number with same count of the max number of one the element
    * double type doesn't exist
    * dtype=str =strings =''
  * matrix_arr=np.array([[1,2,3],[4,5,6]])
  * int_array=np
* add lists: third= first+second=[5,7,9]: adding values
  * must be the same length
* functions:
  * arrange(start,end,jump): create new numpy array with range of numbers:
    * np.arrange(0,5)=[0,1,2,3,4]
    * including start, not including the end
    * jump value: default =1, must be != 0
  * zeros(length):create array with length zeros
    * defaults the type is float=[0. , 0.]
    * can add dtype=int/float,str (not tuple zeros((2,5),dtype=int))
    * for matrix array with zeros: zeros((2,5))= 2 rows, each row 5 zeros
  * reshape(array,(new dimensions)): change the input array new dimensions
    ```
    sh=np.arrange(0,10)
    np.reshape(sh,(2,5)
    ```
    ** dimensions must be sum the same length of the origin array
    ** for 2d array, and don't one of the dimension, set -1, and it will be complete automatically:
    ```
    a.reshape(5,-1) - # 5 rows
    a.reshape(-1,2) - # 2 columns
    ```
  * linspace(start,end,length)= creates array with length elements, between the range start-end 
  * with even jumps according to the length
    * including end number
    * length must be int
    * works as:(start+end)/length
    ```
    linspace(0,10,3)=[0,5,10]
    ```
    * to get float elements: 
    ```
    linspace(0,10,4)=[ 0.          3.33333333  6.66666667 10.        ]
    ```
  * random.rand(length_rows): return random number with range 0-0.999999
    * default length_rows=1, return 1 float number not array =0.3992505617874117
    * length_rows=2 return 1 array with 2 float number=[0.19225449 0.42497501]
    * length_rows=(2,3) return matrix with 2 rows of 3 elements=
       [[0.39190353 0.18186458 0.73266108] ,[0.03607893 0.06987064 0.99566214]]
    * random numbers between 0-10 float =random.rand(length_rows)*9
    * covert to other type=random.rand(length_rows).astype(int)
  * random.randint(start,end,size)=np.random.randint(0,10,2)=[5,8]
  * round(array,numbers count after the .) on all elements :np.round(np.random.rand(2)),2)=[0.76 0.49]
  * random.seed()= to create random numbers evenly: will according to the seed the random function changes
    * will receive the exact same random numbers as other run executions or other people with same function
    * this help for testing and simulations
