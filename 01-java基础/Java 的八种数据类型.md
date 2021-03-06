# Java 中的数据类型

Java 为数值、字符值和布尔值数据提供了八种基本数据类型，它们分别是如下：

|    类型名称  | 存储需要 |  范围   |  存储大小 |
| --------| -----:   | -----:   | :----: |
| byte      | 1 byte = 8 bit | -2<sup>7</sup>(-128) ~ 2<sup>7</sup> - 1(127)     |   8 位带符号数大小   |
| short      | 2 bytes = 16 bit | -2<sup>15</sup>(-32768) ~ 2<sup>15</sup> - 1(32767)     |   16 位带符号数大小   |
| int      | 4 bytes = 32 bit | -2<sup>31</sup>(-2147483648) ~ 2<sup>7</sup> - 1(2147483647)     |   32 位带符号数大小    |
| long      |8 bytes = 64 bit| -2<sup>63</sup> ~ 2<sup>63</sup>-1      |    64 位带符号数大小   |
| float     |4 bytes = 32 bit |       |    32 位，标准 IEEE 754   |
| double     |8 bytes = 64 bit |       |   64 位，标准 IEEE 754   |


Java 中使用四种类型的整数，他们如下：

### 1. 四种整数类型 

byte short int long 它们表示的是带符号的数字。

1. byte 单位是字节，1 byte = 8 bit。也就是说一个字节等于八位二进制数据。它的范围是

2. short 是短整型，1 short = 2 byte = 16 bit

3. int 是整型。 1 int = 4 byte = 32 bit，也就是说是 32 位二进制数据

4. long 是长整型， 1 long = 8 byte = 64 bit。


Java 中使用两种类型的浮点数，他们如下：

### 2. 表示浮点数类型 

float 和 double 

float 表示浮点类型，带有小数点，比如 1.2f 等。double 类型是 float 类型的两倍，所以 double 型又称为双精度浮点型，而 float 称为单精度浮点型。通常的情况下，我们应该使用 double 型，因为 double 型比 float 类型更加精确。



> 浮点型通常带小数点，默认情况下都是 double 类型的。例如 5.0 通常被认为是 double 类型而不是 float 类型，如果我们要指定 5.0 为 float 类型，我们可以尝试在 5.0 后面加上 f 或者 F 来表示该数值类型为 float 类型。
> 
> 也可以在数值后面加上 d 或者 D 来表示该数值为 double 类型。
> 
> 
> **注意：double 类型通常比 float 类型要精确。例如：**
> 
> 1.0 / 3.0 输出的结果是 0.333333333333 （小数点后 16 位）
> 
> 1.0f / 3.0f 输出的结果通常是 0.33333333 （小数点后 8 位） 

## 2. 表示字符类型

char 一般表示一个字符。例如 ‘A‘ 就是一个字符，它对应的 ASCII 码值就为 67，它和 “A” 不同，“A” 表示的是一个字符串，这个字符串的长度为 1。 

## 3. 表示布尔类型

boolean 类型，一般表示 true 或者 false，声明为 boolean 类型的时候，默认赋值为 false。布尔类型通常用来判断逻辑条件。


> Math.random() 返回一个 0.0 到 1.0 之间的随机 double 值，不包括 1.0。



# Java 中基本数据类型对应的包装类

**基本数据类型值不少一个对象，但是可以使用 Java API 中的包装类来包装成一个对象使用。**

出于对性能的考虑，在 Java 中基本数据类型不作为对象使用。因为处理对象需要额外的系统开销，所以，如果将基本数据类型当做对象，就会给语言性能带来负面影响。然而，Java 中的许多方法需要将对象作为参数。 Java 提供了一个方便的办法，即将基本数据烈性并入对象或者包装成对象，一下便是八种基本类型对应的包装类。

> 1. int 对应 Integer 
> 2. byte 对应 Byte
> 3. short 对应 Short
> 4. long 对应 Long
> 5. char 对应 Character
> 6. boolean 对应 Boolean
> 7. float 对应 Float 
> 8. double 对应 Double

通过使用包装类，我们可以将基本数据类型当做对象来处理。

> 注意：大多数基本类型的包装类的名称与对应的基本数据类型名称一样，第一个字母要大写。Integer 和 Character 例外。
> 
> 包装类中没有无参构造方法。所有包装类的实例都是不可改变的，这意味着一旦创建对象后，他们内部的值就不能再改变。


# JDK 1.5 自动装箱与拆箱
根据上下文环境，基本数据类型值可以使用包装类自动转换成一个对象，反过来的自动转换也可以。将基本类型值转换成包装类对象的过程称为 “**装箱**“ 。相反的过程称之为自动拆箱。Java 允许基本类型和包装类型之间进行自动转换。如果一个基本类型值出现在需要对象的环境中，编译器会将基本类型值进行自动装箱；如果一个对象出现在需要基本类型值的环境中，编译器会将对象进行自动开箱。

```java
Integer object = new Integer(2);
Integer intObject = 2;//自动装箱
```


