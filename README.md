# CST211-Lab1-Test
Oregon Institute of Technology
CST 211 Data Structures
Lab 1: Single Dimensional Array


Lab 1
Single Dimensional Array
Description
Write an Array ADT that is based on a dynamic array. Use the following class definition to build your class. You will use the associated test stub to test your classes.
Array UML

Array

          typename T:
          
private:

- m_array: T *
- m_start_index: int
- m_length: int


public:

+ Array()
+ Array(in length:int, in start_index:int=0)
+ Array(in copy:const Array<T> &)
+ Array(inout copy:Array<T> &&)
+ operator =(in rhs:const Array<T> &): Array &
+ operator =(inout rhs:Array<T> &&): Array &
+ ~Array()
+ operator [] (in index:int): T &
+ getStartIndex(): int
+ setStartIndex(in start_index:int): void
+ getLength(): int
+ setLength(in length:int): void


Stipulations
1. Make sure that the length values are valid.
2. Make sure the user never goes out of bounds. If they do, throw an exception (see below).
3. The user should be able to set the length of the array at any time to any valid length, including lengths that are smaller than the current length. This may result in the loss of data, but should still be allowed.
4. The user should have the capability of specifying a negative starting index.
5. You must create and use the following Exception class. This class will be used to handle the following exceptions:
   1. Specifying an index smaller than the lower bounds.
   2. Specifying an index larger than the upper bounds.


Exception UML
private:
- m_msg: char *
public:
+ Exception()
+ Exception(in msg: const char *)
+ Exception(in copy: const Exception &)
+ Exception(inout copy:Exception &&)
+ ~Exception()
+ operator =(in rhs:const Exception &): Exception &
+ operator =(inout rhs:Exception &&): Exception &
+ getMessage(): const char *
+ setMessage(in msh:const char *): void
+ operator <<(inout stream:ostream &, in except:const Exception &): ostream &

Deliverables
One file including:
* Array.h
* Exception.h
* The output from the Lab1_test.cpp run for your code.
