# 判断正整数位数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    给定一个不多于5位的正整数，判断它是几位数，并将该数字输出。输出结束后换行。
  </p>
  
  <p>
    注意：输入的数字要确保是一个不多于5位的正整数。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  一个不多于5位的正整数。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输入正整数的位数，注意末尾的换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int x,i;
    while(scanf("%d",&x)!=EOF){
        while(x!=0){
            x=x/10;
            i=i+1;
        }
        cout&lt;&lt;i&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
