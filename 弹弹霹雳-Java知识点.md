[TOC]

# 一、Java基础

## 1.1 String、StringBuffer、StringBuilder的区别是什么？

### 可变性

String类中使用final关键字修饰字符数组来保存字符串，所以String对象是不可变的。

```java
pirvate final char value[];

//在Java9之后，String类的实现改用byte数组存储字符串
private final byte[] value;
```

StringBuilder与StringBuffer都继承AbstractStringBuilder类，在AbstractStringBuilder中也是使用字符数组保存字符串`char[] value`，但是没有用final关键字修饰，所以这两种对象都是可变的

### 线程安全性

String中的对象是不可变的，也就可以理解为常量，线程安全。

StringBuffer对方法加了同步锁或者对调用的方法加了同步锁，所以是线程安全的。

StringBuilder并没有对方法进行加同步锁，所以是非线程安全的

### 性能

每次对String类型进行改变的时候，都会生成一个新的String对象，然后将指针指向新的String对象。

StringBuilder和StringBuffer每次都会对对象本身进行操作，而不是生成新的对象。

StringBuilder的性能比StringBuffer的性能要好，但是会冒多线程不安全的风险

###  使用总结

1. 操作少量的数据：适用String
2. 单线程操作字符串并操作大量数据：适用StringBuilder
3. 多线程操作字符串并操作大量数据：使用StringBuffer