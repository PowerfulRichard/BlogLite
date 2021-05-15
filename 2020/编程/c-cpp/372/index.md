# 冒泡排序

## 题目描述 {.page-header.text-muted}

<div class="content">
  从键盘上输入10个整数，用冒泡法对这10个数进行排序（由小到大）。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  以空格分隔的10个整数
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  依次输出排好序的10个整数，每个数占一行。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a[10];
    int i,j,t;
    for(i=0; i&lt;10; i++)
        scanf("%d",&a[i]);
    for(j=0; j&lt;9; j++)
        for(i=0; i&lt;9-j; i++)
            if(a[i]&gt;a[i+1]) {
                t=a[i];
                a[i]=a[i+1];
                a[i+1]=t;
            }
    for(i=0; i&lt;10; i++)
        printf("%d ",a[i]);
}</pre>

&nbsp;
