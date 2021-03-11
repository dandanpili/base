[TOC]

# SpringBoot知识点

##  一、ResponseBodyAdvice接口

---

###  1、作用

该接口可以将Controller接口返回的数据进行拦截，再根据你业务情况，可以定义一些所有返回值都必须要带的一些属性，进行一层保证，从而减少代码的冗余。

### 2、使用方法

先定义一个类，实现ResponseBodyAdvice<>接口，然后在实现该接口的类上添加@ControllerAdvice注解，该注解可以设置一些属性，来设置要扫描的包和类。

之后重写**supports**方法和**beforeBodyWrite**方法;

**support**方法用来注明哪些方法需要支持Controller返回时，再做一层封装

**beforeBodyWrite**方法用来注明进行何种封装，该方法就由用户自定义了。

###  3、例子

```

```



