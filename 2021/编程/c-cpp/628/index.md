# 阶乘之和

## 题目描述 {.page-header.text-muted}

<div class="content">
  给你一个非负数整数n，判断n是不是一些数（这些数不允许重复使用，且为正数）的阶乘之和，如9=1！+2!+3!，如果是，则输出Yes，否则输出No；
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行有一个整数0<m<100,表示有m组测试数据；<br /> 每组测试数据有一个正整数n<1000000;
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  如果符合条件，输出Yes，否则输出No
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int jc(int n)
{
    int b=1;
    for(int i=1;i&lt;=n;i++)
        b*=i;
        return b;
}
int main()
{
    int n; scanf("%d",&n);
    while(n--)
    {
        int m,b;
        scanf("%d",&m);
    for(int i=10;i&gt;0;i--)
    {
        if(m&gt;=jc(i)&&m&gt;0)
        m-=jc(i);
        if(m==0)
         b=1;
        else
         b=0;
    }
    if(b==1)
    printf("Yes\n");
    else
    printf("No\n");
    }
    return 0;
}</pre>

&nbsp;
