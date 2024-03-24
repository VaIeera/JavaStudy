## List Overview

* （1）ArrayList：底层数据结构是数组，查询快，增删慢，线程不安全，效率高，可以存储重复元素  
* （2）LinkedList 底层数据结构是链表，查询慢，增删快，线程不安全，效率高，可以存储重复元素  
* （3）Vector:底层数据结构是数组，查询快，增删慢，线程安全，效率低，可以存储重复元素  

### ArrayList

```       java
String[] fruits = {"apple", "orange", "banana", "lemon", "watermelon"};
List<String> fruitList = new ArrayList<(Arrays.asList(fruits));
System.out.println(fruitList);
```

#### 1. add( )  

在集合末尾添加元素；

```java
  fruitList.add("cherry");
```



在指定位置添加元素；

```java
  fruitList.add(1,"cherry");
```

#### 2.addAll( )



