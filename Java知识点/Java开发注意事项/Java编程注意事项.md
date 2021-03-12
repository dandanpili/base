[TOC]

#  Java编程注意事项

------

##  一、工具类的注意事项

###  1、使用Deque的注意事项(用Deque代替Stack)

Deque是双端队列接口，其实现类有**LinkedList**，**ArrayDeque**，**LinkedBlockingDeque**；

使用Deque进行插入或者删除或者检查时，**最好注明操作方向**，否则容易因为取出或插入方向不明确而导致操作失误。

|              |      抛出异常      |    返回null     |     抛出异常      |    返回null    |
| :----------: | :------------: | :-----------: | :-----------: | :----------: |
|    **插入**    |  addFirst( )   | offerFirst( ) |  addLast( )   | offerLast( ) |
|    **删除**    | removeFirst( ) | pollFirst( )  | removeLast( ) | pollLast( )  |
| **检查（不会删除）** |  getFirst( )   | peekFirst( )  |  getLast( )   | peekLast( )  |

要使用栈结构时，优先选择Deque，然后在队列的同一端进行操作，不应该使用遗留类Stack

|  堆栈方法   |   等效Deque方法    | 操作失败时 |
| :-----: | :------------: | :---: |
| push( ) |  addFirst( )   | 抛出异常  |
| pop( )  | removeFirst( ) | 抛出异常  |
| peek( ) |  peekFirst( )  | 抛出异常  |

Queue中相关操作对应于Deque中的操作

| Queue方法(FIFO先进先出) |   等效Deque方法   |
| :---------------: | :-----------: |
|      add( )       |  addLast( )   |
|     offer( )      | offerLast( )  |
|     remove( )     | removeLast( ) |
|      poll( )      |  pollLast( )  |
|    element( )     |  getFirst( )  |
|      peek( )      | peekFirst( )  |

## 二、判断语句的注意事项

### 1、使用switch语句判断

switch语句不能对null值进行判断，会报空指针异常。





