# 五次方数

## 问题描述

对一个数十进制表示时的每一位数字乘五次方再求和，会得到一个数的五次方数

  * 例如：1024的五次方数为1+0+32+1024=1057

有这样一些神奇的数，它的五次方数就是它自己，而且这样的数竟然只有有限多个

从小到大输出所有这样的数

## 输入

无

## 输出

每个数独立一行输出

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;iostream&gt;
using namespace std;
int n;
int wucifang(int x){
    return x*x*x*x*x;
}
 
int main()
{
    for(int i=2;i&lt;=194980;i++){
        int sum=0,t=i;
        while(t){
            sum+=wucifang(t%10);
            t/=10;
        }
        if(sum==i)
        cout&lt;&lt;i&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
