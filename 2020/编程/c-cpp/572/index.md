# 折半插入排序

<h2 style="font-weight: 500;">
  题目描述
</h2>

折半插入排序同样是一种非常简单的排序方法，它的基本操作是在一个已经排好序的有序表中进行查找和插入。不难发现这个查找的过程可以十分自然的修改成折半查找的方式进行实现。

折半插入排序的算法可以描述如下：

在本题中，读入一串整数，将其使用以上描述的折半插入排序的方法从小到大排序，并输出。

<h2 style="font-weight: 500;">
  输入
</h2>

输入的第一行包含1个正整数n，表示共有n个整数需要参与排序。其中n不超过1000。

第二行包含n个用空格隔开的正整数，表示n个需要排序的整数。

<h2 style="font-weight: 500;">
  输出
</h2>

只有1行，包含n个整数，表示从小到大排序完毕的所有整数。

请在每个整数后输出一个空格，并请注意行尾输出换行。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int a[1005];
int main(){
    int  n;
    cin&gt;&gt;n;
    for(int i=0;i&lt;n;i++) cin&gt;&gt;a[i];
    int low,high,mid;
    for(int i=1;i&lt;n;i++){
        int low=0;high=i-1;
        int k=a[i];
        while(low&lt;=high){
            mid=(low+high)&gt;&gt;1;
            if(a[i]&lt;a[mid]) high=mid-1;
            else
            low =mid+1;
        }
        for(int j=i;j&gt;=low+1;j--) a[j]=a[j-1];
        a[low]=k;
    }
    for(int i=0;i&lt;n;i++) cout&lt;&lt;a[i]&lt;&lt;" ";
    cout&lt;&lt;endl;
    return 0;
}</pre>

&nbsp;
