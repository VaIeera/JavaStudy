## Array是数组
     Java中最基本的一个存储结构。

     提供了动态创建和访问 Java 数组的方法。其中的元素的类型必须相同。

     效率高，但容量固定且无法动态改变。

     它无法判断其中实际存有多少元素，length只是告诉我们array的容量。


## 静态类Arrays  

此静态类专门用来操作array ，提供搜索、排序、复制等静态方法。

      equals()：比较两个array是否相等。array拥有相同元素个数，且所有对应元素两两相等。

      sort()：用来对array进行排序。

      binarySearch()：在排好序的array中寻找元素。

      Arrays.asList(array):将数组array转化为List
