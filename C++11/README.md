# Cplusplus
c++11基本的编程技巧
C++中的容器大致可以分为两个大类：顺序容器和关联容器。顺序容器中有包含有顺序容器适配器。

顺序容器：将单一类型元素聚集起来成为容器，然后根据位置来存储和访问这些元素。主要有vector、list、deque（双端队列）。顺序容器适配器：stack、queue和priority_queue。
关联容器：支持通过键来高效地查找和读取元素。主要有：pair、set、map、multiset和multimap。

一. 顺序容器

1.顺序容器定义

为了定义一个容器类型的对象，必须先包含相关的头文件：

   定义vector：#include <vector>  vector<int> kk;

   定义list：#include <list>     list<int> kk;

   定义deque：#include <deque>    deque<int> kk;
    
2.容器的选用

选择容器类型的常规法则：

①如果程序要求随机访问元素，则应使用 vector 或 deque 容器。
②如果程序必须在容器的中间位置插入或删除元素，则应采用 list 容器。
③如果程序不是在容器的中间位置，而是在容器首部或尾部插入或删除元素，则应采用 deque 容器。
④如果只需在读取输入时在容器的中间位置插入元素，然后需要随机访问元素，则可考虑在输入时将元素读入到一个 list 容器，接着对此容器重新排序，使其适合顺序访问，然后将排序后的 list 容器复制到一个 vector容器。
如果程序既需要随机访问又必须在容器的中间位置插入或删除元素，选择何种容器取决于下面两种操作付出的相对代价：随机访问 list 容器元素的代价，以及在 vector 或 deque 容器中插入／删除元素时复制元素的代价。通常来说，应用中占优势的操作（程序中更多使用的是访问操作还是插入／删除操作）将决定应该什么类型的容器。


二.关联容器

1.pair

2.map

3.set

4.multimap ,multiset


* [数据结构](http://lotleaf.com/algorithm/algorithm-exercises-answer-1.html)
