# 判断素数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    输入一个大于等于3的正整数，判断其是否是素数。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    一个大于等于3并小于10000的正整数n，判断n是否是素数。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    如果n是素数，输出“prime”，否则请输出“not prime”。<br /> 请注意不需要输出引号，行尾输出换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,a=0;
    scanf("%d",&n);
    for(int i=1;n&gt;i;i++){
        if(n%i==0){
            a++;
        }
    }
    if(a==1){
        cout&lt;&lt;"prime"&lt;&lt;endl;
    }
    else{
        cout&lt;&lt;"not prime"&lt;&lt;endl;
    }
    
    return 0;
}</pre>

&nbsp;
