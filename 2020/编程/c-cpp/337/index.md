# 求正整数各位上的数字

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    输入一个不多于5位的正整数，按高位到低位的顺序输出各位上的数字，末尾换行。
  </p>
  
  <p>
    注意：确保输入的正整数的位数不多于5。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  一个不多于5位的正整数
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    从高位到低位依次输出各位上的数字，中间以空格分隔的。
  </p>
  
  <p>
    注意末尾的换行。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int x,t;
    cin&gt;&gt;x;
    if(x&gt;9999){
        t=x;
        t=t/10000;
        cout&lt;&lt;t&lt;&lt;" ";
        x=x%10000;
    }
    if(x&gt;999&&x&lt;=9999){
        t=x;
        t=t/1000;
        cout&lt;&lt;t&lt;&lt;" ";
        x=x%1000;       
    }
    if(x&gt;99&&x&lt;=999){
        t=x;
        t=t/100;
        cout&lt;&lt;t&lt;&lt;" ";
        x=x%100;        
    }
    if(x&gt;9&&x&lt;=99){
        t=x;
        t=t/10;
        cout&lt;&lt;t&lt;&lt;" ";
        x=x%10;     
    }
    cout&lt;&lt;x&lt;&lt;endl; 
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
