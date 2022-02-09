### java 笔记

##### 小驼峰命名法：方法和变量

标识符是单一单词时首字母小写，标识符由多个单词组成时，第一个单词首字母小写其他单词首字母大写，如name，firstName

##### 大驼峰命名法：类

标识符是单一单词时首字母大写，标识符由多个单词组成时，每个单词首字母大写，如Student和GoodStudent

##### 字符串拼接

```java
System.out.println("zyz"+66+6)
//输出zyz666
System.out.println(66+6+"zyz")
//输出72zyz
System.out.println(666+"zyz")
//输出666zyz
System.out.println("zyz"+666)
//输出666zyz
```

##### s+=20和s=s+20的区别

```java
int s=10
//s+=20，s=s+20等价
short s=10
//s+=20，s=s+20不等价，因为s=s+20会报错而s+=20不会，20默认是int类型的，而s是short类型则无法相加
```

java会自动转换变量类型，如

```java
public static String getType(Object o) { //获取变量类型方法
        return o.getClass().toString(); //使用int类型的getClass()方法
    }
short s=10;
System.out.println(getType(s));
System.out.println(getType(s+10));
//输出结果class java.lang.Short
//class java.lang.Integer
```

#### 数组初始化

##### 数组定义:

```java
int[] arr
int arr[]
```

##### 数组初始化

```java
//动态初始化
int[] arr=new int[3]
//数组在初始化的时候会为存储空间添加默认值，其中整数的默认值为0，浮点数的默认值为0.0，布尔值的默认值是false，字符的默认值为空字符，引用数据类型的默认值为null
    
//数组静态初始化
int[] arr=new int[]{1,2,3};
//简化写法
int[] arr={1,2,3};
```

##### java中的内存分配

栈内存储存局部变量，而堆内存存储new出来的内(实体与对象)

栈内存储存局部变量，定义在方法中的变量，例如arr，使用完毕立刻消失

堆内存存储new出来的内容如(实体与对象)

##### 方法重载的要求

1. 多个方法在同一个类中

2. 多个方法具有相同的方法名

3. 多个方法的参数不相同，类型不相同或者数量不同

   ##### java文件前的package引起的错误

   参照博客https://zhuanlan.zhihu.com/p/363810605

如果在类名前未申明package，则![image-20220209205614790](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220209205614790.png)

倘若在java文件前加了package的申明，则按照上述命令行将会报错，需要将命令行改为:![image-20220209205839633](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220209205839633.png)

![image-20220209232439861](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220209232439861.png