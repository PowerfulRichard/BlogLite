# 逆序输出正整数各位上数字

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    输入一个不多于5位的正整数，按逆序输出各位上的数字，末尾换行。
  </p>
  
  <p>
    注意：确保输入的正整数的位数不多于5。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  一个不多于5位的正整数。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    逆序输出各位上的数字，中间以空格分隔。
  </p>
  
  <p>
    注意末尾的换行。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int x,t;
    cin&gt;&gt;x;
    while(x!=0){
        t=x;
        cout&lt;&lt;t%10&lt;&lt;" ";
        x=x/10;
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
