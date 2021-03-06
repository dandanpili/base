## Java开发注意事项

1、如果改动会影响方法的返回值，需要考虑一下该方法名是否需要修改，以表达你返回值所代表的意思

2、前后端分离的情况下，后端如果是要修改接口，需要思考该接口能否兼容旧版本，如果不能兼容，需要新创建一个接口来实现当下的功能，老接口用@Deprecated注释，以便下个版本开发时，提示应该删除哪些老接口。

3、如果要寻找数据库表到底在项目的哪些地方做了修改，可以搜索该数据库表对应的实体类在哪些地方做了实例化，先查看该类到底有几种实例化方式，例如构造方法、builder、of等...，在IDEA中通过Ctrl + H唤出Find in Path，例如实体类是User，查构造方法就查：new User，查builder就查：user.builder ，查 of就查 user.of （大前提是，遵循代码规范，User的实体类都叫user），也可以查看UserDao类对数据库进行的插入和更新操作，然后自下而上的寻找有关该表的相关操作

4、如果需要根据多个字段去匹配某一个具体的值，可以将该多个字段封装到一个类中，然后实现equal和hashCode方法，然后可以以该类的实例作为一个键，去查找对应的值。