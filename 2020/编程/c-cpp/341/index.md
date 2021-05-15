# 求最小公倍数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    写一个函数求两个整数的最小公倍数，通过主函数调用这个函数，并输出结果。
  </p>
  
  <p>
    两个整数由键盘输入。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  以空格分隔的两个整数
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输入两数的最小公倍数，单独占一行。
</div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int x,y,n=1;
    cin&gt;&gt;x&gt;&gt;y;
    while(n%x!=0||n%y!=0){
        n++;
    }
    cout&lt;&lt;n;
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
