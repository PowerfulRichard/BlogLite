# 水仙花问题（4）

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    输出区间[a,b]中的所有水仙花数，若三位数ABC满足ABC=A^3+B^3+C^3,则称为水仙花数。例如153=1^3+5^3+3^3，所以 153是水仙花数
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    一个区间【a,b】,b,a都是非负整数 且满足b＞ａ＞０
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出区间[a,b】中的所有水仙花数（每一个１行）
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,b,c,x,y;
    cin&gt;&gt;x&gt;&gt;y;
    while(x&lt;y){
        a = x % 10;
        b = ((x % 100) - a) / 10;
        c = (((x % 1000) - a) - 10 * b) / 100;
        if (x == (a * a * a) + (b * b * b) + (c * c * c)){
            cout&lt;&lt;x&lt;&lt;endl;
        }
        x=x+1;a=0;b=0;c=0;
    }
    
    return 0;
}</pre>

&nbsp;
