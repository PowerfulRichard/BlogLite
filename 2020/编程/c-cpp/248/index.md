# 被3和5整除的数

## 题目描述 {.page-header.text-muted}

<div class="content">
  计算从 m 到 n 能同时被3和5整除的数的个数
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入两个整数 m, n ( 0 < m <= n < 10000 )。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出从 m 到 n 能同时被3和5整除的数的个数
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,m,i=0;
    cin&gt;&gt;m&gt;&gt;n;
    while(m&lt;=n){
        if(m%3==0&&m%5==0){
            i++;
        }
        m++;
    }
    cout&lt;&lt;i&lt;&lt;endl;
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
