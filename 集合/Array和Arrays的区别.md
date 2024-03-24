## Array是数组
Java中最基本的一个存储结构。

提供了动态创建和访问 Java 数组的方法。其中的元素的类型必须相同。

效率高，但容量固定且无法动态改变。

它无法判断其中实际存有多少元素，length只是告诉我们array的容量。


## 静态类Arrays  

此静态类专门用来操作array ，提供搜索、排序、复制等静态方法。



### 1. Arrays.equals( )：比较两个array是否相等。array拥有相同元素个数，且所有对应元素两两相等。
>boolean isSame = Arrays.equals(a,b);
>注意：Arrays.equals()是比较数组内容，而a.equals(b) 这样的方法是比较地址值



### 2. Arrays.sort( )：用来对array进行排序。
>int[ ] a = new int[5]{5，4，3，2，1};  
>Arrays.sort(a); // 1 2 3 4 5  
>System.out.println(Arrays.toString(a));  
>// [1,2,3,4,5]  

如果要实现降序排列
#### * Collections.reverseOrder ()
>Integer[ ] a = {1,2,3,4,5}  
>Arrays.sort(a,Collections.reverseOrder( ))  
>// 输出数组的内容即为：5 4 3 2 1    
注意这里使用Integer[ ]而非int[ ]，如果用int数组，它会提示你：“需要的是一个泛型T[ ]，而不是int[ ]” （这里不做讲解，你只要知道不能int就行了）
  
#### * 实现Comparator接口

![](https://img-blog.csdnimg.cn/0e3ad1130adb4670afadb93814ff8e92.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCP5L2V4pSM,size_20,color_FFFFFF,t_70,g_se,x_16)

### 3. binarySearch( )：在排好序的array中寻找元素。方法作用：在数组中查找元素  
>int Arrays.binarySearch( Datatype[], Datatype key)  
在数组中查找指定值，若找到，则返回此值的下标，

若没找到，返回 -插入点-1；

>int[] a = {1,5,6,7};
>Arrays.binarySearch(a,2)  //没找到，插入点为1，则返回 -2  
>Arrays.binarySearch(a,4)  //没找到，插入点为1，则返回 -2  
>Arrays,binarySearch(a,8)  //没找到，插入点为4，则返回 -5  
>Arrays.binarySearch(a,5)  //找到了！返回下标 1  
只要返回值 ≥ 0 ，就代表找到了。

### 4. Arrays.asList(array):将数组array转化为List

### 5. Arrays.toString（）：快速输出数组内容，可以偷偷懒。
>int[ ] a = {1,2,3,4,5};  
>System.out.println(Arrays.toString(a));  
>// 输出格式：[1,2,3,4,5]

### 6.  Arrays.copyOf()作用：拷贝数组  
>public static void main(String[] args) {  
>        int[] arr1 = new int[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};  
>        int[] arr2 = new int[5];  
>        arr2 = Arrays.copyOf(arr1, 10);  
>}
rrays.copyOf()的拷贝是从下标0开始的，如果你想从其他下表开始，可以使用Arrays.copyOfRange()方法  
>// from 表示开始位置， to 表示结束位置    
>// 复制下标为 ：[from, to)  
>Arrays.copyOfRange(int[] original, int from, int to)
比如：
>arr2 = Arrays.copyOfRange(arr1, 2，5);
表示拷贝下标[2,5)，即下表为2，3，4被拷贝到arr2
>


