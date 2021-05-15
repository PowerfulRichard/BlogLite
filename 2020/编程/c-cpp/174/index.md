# Repetitive Processing – How Many Divisors?

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    How Many Divisors?
  </p>
  
  <p>
    Write a program which reads three integers a, b and c, and prints the number of divisors of c between a and b.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  Three integers a, b and c are given in a line separated by a single space.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Print the number of divisors in a line.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,b,c,i=0;
    scanf("%d %d %d",&a,&b,&c);
    while(a&lt;=b){
        if(c%a==0){
            i=i+1;
        }
        a=a+1;
    }
    cout&lt;&lt;i&lt;&lt;endl;
    
    return 0;
}</pre>

&nbsp;
