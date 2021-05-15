# 火柴棒等式

## 题目描述 {.page-header.text-muted}

<div class="content">
  <div align="left">
    给你n根火柴棍，你可以拼出多少个形如“A+B=C”的等式？等式中的A、B、C是用火柴棍拼出的整数（若该数非零，则最高位不能是0）。用火柴棍拼数字0-9的拼法如图所示：
  </div>
  
  <div align="left">
    <img loading="lazy" id="aimg_E4e4Z" class="zoom" src="https://i0.wp.com/bbs.tianchai.org/data/attachment/forum/201312/23/175556vzverplrdlv6rqlq.jpg?resize=500%2C84" alt="" width="500" height="84" border="0" data-recalc-dims="1" />
  </div>
  
  <div align="left">
    注意：
  </div>
  
  <div align="left">
    1. 加号与等号各自需要两根火柴棍
  </div>
  
  <div align="left">
    2. 如果A≠B，则A+B=C与B+A=C视为不同的等式（A、B、C>=0）
  </div>
  
  <div align="left">
    3. n根火柴棍必须全部用上
  </div>
</div>

## 输入 {.page-header.text-muted}

只有一行，有一个整数n（n<=24）。

## 输出 {.page-header.text-muted}

只有一行，表示能拼成的不同等式的数目。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int g[10]={6,2,5,5,4,5,6,3,7,6};
int main()
{
    int s=0,n,a=0,b=0,c=0;
    cin&gt;&gt;n;
    for(int i=0;i&lt;=1000;i++)
    {
        for(int j=0;j&lt;1000;j++)
        {
            int k=i,p=j,m=i+j;
            if(k==0)a=6;
            else while(k&gt;0){a+=g[k%10];k=k/10;}
            if(p==0)b=6;
            else while(p&gt;0){b+=g[p%10];p=p/10;}
            if(m==0)c=6;
            else while(m&gt;0){c+=g[m%10];m=m/10;}
            if((a+b+c)==(n-4))s++;
            a=0;b=0;c=0;
        }
    }
    cout&lt;&lt;s;
    return 0;
}</pre>

&nbsp;
