# 数组的距离

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    已知元素从小到大排列的两个数组f[]和g[]，请写出一个程序算出两个数组彼此之间差的绝对值中最小的一个，这叫做数组的距离
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    第一行为两个整数m, n(1≤m, n≤1000)，分别代表数组f[], g[]的长度。<br /> 第二行有m个元素，为数组f[]。<br /> 第三行有n个元素，为数组g[]。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    数组的最短距离
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int abs(int s);          
int main()
{
    int a[10000],b[10000],c,d,i,n,min=99999,t;
    cin&gt;&gt;c&gt;&gt;d;
    for(i=0;i&lt;c;i++)
    {
        cin&gt;&gt;a[i];
    }
    for(n=0;n&lt;d;n++)
    {
        cin&gt;&gt;b[n];
    }
    for(i=0;i&lt;c;i++)
    {
        for(n=0;n&lt;d;n++)
        {
            t=abs(a[i]-b[n]);
            if(t&lt;min)
                {
                    min=t;
                }
        }
    }
    cout&lt;&lt;min;
    return 0;
}
int abs(int s)
{
    if(s&lt;0)
    return -s;
    else
    return s;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
