# Assignment-1noticed that some numpy operations take an argument called shape, such as np.zeros, whereas some others take an argument called size, such as np.random.randint. To me, those arguments have the same function and the fact that they have different names is a bit confusing. Actually, size seems a bit off since it really specifies the .shape of the output.

Is there a reason for having different names, do they convey a different meaning even though they both end up being equal to the .shape of the outputThe term broadcasting refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations. Arithmetic operations on arrays are usually done on corresponding elements. If two arrays are of exactly the same shape, then these operations are smoothly performed.

Example 1

") no-repeat;">Live Demo

import numpy as np a = np.array([1,2,3,4]) b = np.array([10,20,30,40]) c = a * b print c

Its output is as follows −

[10 40 90 160] 

If the dimensions of two arrays are dissimilar, element-to-element operations are not possible. However, operations on arrays of non-similar shapes is still possible in NumPy, because of the broadcasting capability. The smaller array is broadcast to the size of the larger array so that they have compatible shapes.

Broadcasting is possible if the following rules are satisfied −

Array with smaller ndim than the other is prepended with '1' in its shape.

Size in each dimension of the output shape is maximum of the input sizes in that dimension.

An input can be used in calculation, if its size in a particular dimension matches the output size or its value is exactly 1.

If an input has a dimension size of 1, the first data entry in that dimension is used for all calculations along that dimension.

A set of arrays is said to be broadcastable if the above rules produce a valid result and one of the following is true −

Arrays have exactly the same shape.

Arrays have the same number of dimensions and the length of each dimension is either a common length or 1.

Array having too few dimensions can have its shape prepended with a dimension of length 1, so that the above stated property is true.

The following program shows an example of broadcasting.

Example 2

") no-repeat;">Live Demo

import numpy as np a = np.array([[0.0,0.0,0.0],[10.0,10.0,10.0],[20.0,20.0,20.0],[30.0,30.0,30.0]]) b = np.array([1.0,2.0,3.0]) print 'First array:' print a print '\n' print 'Second array:' print b print '\n' print 'First Array + Second Array' print a + b

The output of this program would be as follows −

First array: [[ 0. 0. 0.] [ 10. 10. 10.] [ 20. 20. 20.] [ 30. 30. 30.]] Second array: [ 1. 2. 3.] First Array + Second Array [[ 1. 2. 3.] [ 11. 12. 13.] [ 21. 22. 23.] [ 31. 32. 33.]]The term broadcasting refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations. Arithmetic operations on arrays are usually done on corresponding elements. If two arrays are of exactly the same shape, then these operations are smoothly performed.

Example 1
Live Demo
import numpy as np 

a = np.array([1,2,3,4]) 
b = np.array([10,20,30,40]) 
c = a * b 
print c
Its output is as follows −

[10   40   90   160]
If the dimensions of two arrays are dissimilar, element-to-element operations are not possible. However, operations on arrays of non-similar shapes is still possible in NumPy, because of the broadcasting capability. The smaller array is broadcast to the size of the larger array so that they have compatible shapes.

Broadcasting is possible if the following rules are satisfied −

Array with smaller ndim than the other is prepended with '1' in its shape.

Size in each dimension of the output shape is maximum of the input sizes in that dimension.

An input can be used in calculation, if its size in a particular dimension matches the output size or its value is exactly 1.

If an input has a dimension size of 1, the first data entry in that dimension is used for all calculations along that dimension.

A set of arrays is said to be broadcastable if the above rules produce a valid result and one of the following is true −

Arrays have exactly the same shape.

Arrays have the same number of dimensions and the length of each dimension is either a common length or 1.

Array having too few dimensions can have its shape prepended with a dimension of length 1, so that the above stated property is true.

The following program shows an example of broadcasting.

Example 2
Live Demo
import numpy as np 
a = np.array([[0.0,0.0,0.0],[10.0,10.0,10.0],[20.0,20.0,20.0],[30.0,30.0,30.0]]) 
b = np.array([1.0,2.0,3.0])  
   
print 'First array:' 
print a 
print '\n'  
   
print 'Second array:' 
print b 
print '\n'  
   
print 'First Array + Second Array' 
print a + b
The output of this program would be as follows −

First array:
[[ 0. 0. 0.]
 [ 10. 10. 10.]
 [ 20. 20. 20.]
 [ 30. 30. 30.]]

Second array:
[ 1. 2. 3.]

First Array + Second Array
[[ 1. 2. 3.]
 [ 11. 12. 13.]
 [ 21. 22. 23.]
 [ 31. 32. 33.]]
 defined prototypes
Task Parallelism
Data Parallelism
Message cursory using M.P.I (Message Passing Interface)
Multiple programs, multiple data (MIMD) parallelism
A single program, multiple data (SPMD) parallelism
4| Numeric Python (Fundamental Numeric Package)
Better known as Numpy, numeric Python has developed a module for Python, mostly written in C.  Numpy guarantees swift execution as it is accumulated with mathematical and numerical functions.

Robust Python with its dynamic data structures, efficient implementation of multi-dimensional arrays and matrices, Numpy assures accurate calculations with matrices and arrays.

We need to import Numpy into memory to perform numerical operations.

Import numpy as np (to import Numpy into memory)
A_values=[20,30,40,50] (defining a list)
A=np.array(A_values) (to convert list into one dimensional numpy array)
print(A) (to get one dimensional array displayed)
print(A*9/5 +32) (to turn values in the list into degrees fahrenheit)
5| Natural Language Toolkit (Library For Mathematical And Text Analysis)
Simply known as NLP, Natural Language Processing library is used to build applications and services that can understand and analyse human languages and data. One of the sub-libraries which are widely used in NLP is NLTK (Natural Language Toolkit). It has an active discussion forum through which they give hands-on guidance on programming basic topics such as computational linguistics, comprehensive API documentation, linguistics to engineers, students, industries and researchers. NLTK is an open source free community-driven project which is accessible for operating systems such as Windows, MAC OS X, and Linux. The implementations of NLP are:

 Search engines (eg: Yahoo, Google, firefox etc) they use NLP to optimise the search results for users.
Social websites like Facebook, Twitter use NLP for the news feed. The NLP algorithms understand the interests of the users and show related posts.
Spam filters: unlike the traditional spam filters, the NLP has driven spam filters to understand what the mail is about and decides whether it is a spam or not.
NLP includes well known and advanced sub-libraries which are very effective in mathematical calculations.

  NLTK, which handles text analysis and related problems. Having over 50 corpora and lexicons, 9 stemmers and handful of algorithms NLTK is very popular for education and research. The    application involves a deep learning and analysing process which makes it one of the tough libraries in NLP
TextBlob, which is a simple library for text analysis
Stanford core NLP, a library that includes entity recognition, pattern understanding, parsing, tagging etc.
SpaCy, which presents the best algorithm for the purpose
Gensim, which is used for topic prototypes and document similarity analysis
NumPy introduces a simple file format for ndarray objects. This .npy file stores data, shape, dtype and other information required to reconstruct the ndarray in a disk file such that the array is correctly retrieved even if the file is on another machine with different architecture.

numpy.save()

The numpy.save() file stores the input array in a disk file with npy extension.

import numpy as np a = np.array([1,2,3,4,5]) np.save('outfile',a)

To reconstruct array from outfile.npy, use load() function.

import numpy as np b = np.load('outfile.npy') print b 

It will produce the following output −

array([1, 2, 3, 4, 5]) 

The save() and load() functions accept an additional Boolean parameter allow_pickles. A pickle in Python is used to serialize and de-serialize objects before saving to or reading from a disk file.

savetxt()

The storage and retrieval of array data in simple text file format is done with savetxt() and loadtxt() functions.

Exampleimport numpy as np a = np.array([1,2,3,4,5]) np.savetxt('out.txt',a) b = np.loadtxt('out.txt') print b 

It will produce the following output −

[ 1. 2. 3. 4. 5.] 

The savetxt() and loadtxt() functions accept additional optional parameters such as header, footer, and delimiter.
numpy.empty() in Python

The numpy module of Python provides a function called numpy.empty(). This function is used to create an array without initializing the entries of given shape and type.

Just like numpy.zeros(), the numpy.empty() function doesn't set the array values to zero, and it is quite faster than the numpy.zeros(). This function requires the user to set all the values in the array manually and should be used with caution.

Syntax

numpy.empty(shape, dtype=float, order='C')  

Parameters:

shape: int or tuple of ints

This parameter defines the shape of the empty array, such as (3, 2) or (3, 3).

dtype: data-type(optional)

This parameter defines the data type, which is desired for the output array.

order: {'C', 'F'}(optional)

This parameter defines the order in which the multi-dimensional array is going to be stored either in row-major or column-major. By default, the order parameter is set to 'C'.


