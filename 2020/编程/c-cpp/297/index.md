# 找零钱

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    在售货员向顾客找零钱时，一般都是尽可能找最少数量的钱币给顾客。下面将给出一定数额的人民币，请将其分解为数量最少的货币。货币单位仅有100 50 20 10 5 2 1几个币种。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    一个整数，即人民币总额（单位元)
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    分解后的人民币序列，用回车分隔
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n;
    cin&gt;&gt;n;
    while(n&gt;0){
        if(n&gt;=100){
            cout&lt;&lt;"100"&lt;&lt;endl;
            n=n-100;
            continue;
        }
        if(n&gt;=50){
            cout&lt;&lt;"50"&lt;&lt;endl;
            n=n-50;
            continue;
        }
        if(n&gt;=20){
            cout&lt;&lt;"20"&lt;&lt;endl;
            n=n-20;
            continue;
        }
        if(n&gt;=10){
            cout&lt;&lt;"10"&lt;&lt;endl;
            n=n-10;
            continue;
        }
        if(n&gt;=5){
            cout&lt;&lt;"5"&lt;&lt;endl;
            n=n-5;
            continue;
        }
        if(n&gt;=2){
            cout&lt;&lt;"2"&lt;&lt;endl;
            n=n-2;
            continue;
        }
        if(n&gt;=1){
            cout&lt;&lt;"1"&lt;&lt;endl;
            n=n-1;
            continue;
        }
    }
    return 0;
}</pre>

&nbsp;
