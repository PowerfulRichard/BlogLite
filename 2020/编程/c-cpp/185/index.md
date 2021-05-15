# A+B

## 题目描述 {.page-header.text-muted}

<div class="content">
  Your task is to calculate the sum of some integers.
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  Input contains an integer N in the first line, and then N lines follow. Each line starts with a integer M, and then M integers follow in the same line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  For each group of input integers you should output their sum in one line, and with one line of output for each line in input.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,sum=0,a;
    while(scanf("%d",&n)!=EOF){
        while(n&gt;0){
            scanf("%d",&a);
            n=n-1;
            sum=sum+a;
        }
        cout&lt;&lt;sum&lt;&lt;endl;
        sum=0;
    }
    return 0;
}</pre>

&nbsp;
