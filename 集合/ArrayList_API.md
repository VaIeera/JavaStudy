## ArrayList

### ListOverview
* （1）ArrayList：底层数据结构是数组，查询快，增删慢，线程不安全，效率高，可以存储重复元素  
* （2）LinkedList 底层数据结构是链表，查询慢，增删快，线程不安全，效率高，可以存储重复元素  
* （3）Vector:底层数据结构是数组，查询快，增删慢，线程安全，效率低，可以存储重复元素  



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

##### `addAll(Collection<? extends E> c)` 

##### `addAll(int index,  Collection<? extends E> c)` 

> 里边是集合，用Arrays.asList( )将数组导入  

#### sort( )
类似Arrays.sort( )
```java
        fruitList.sort(new Comparator<String>() {
            @Override
            public int compare(String o1, String o2) {
                int c1 = o1.toCharArray()[0];
                int c2 = o2.toCharArray()[0];
                return new Integer(c1).compareTo(new Integer(c2));
            }
        });
        System.out.println(fruitList);
```
#### get（ ）
#### set（ ）
#### indexOf（ ）
#### contains( )
#### containsAll( )
#### remove( )
#### toArray( )

### Vector
### LinkedList
