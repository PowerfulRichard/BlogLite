# Array – Reversing Numbers

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Reversing Numbers
  </p>
  
  <p>
    Write a program which reads a sequence and prints it in the reverse order.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input is given in the following format:
  </p>
  
  <p>
    n
  </p>
  
  <p>
    a1 a2 . . . an
  </p>
  
  <p>
    n is the size of the sequence and ai is the ith element of the sequence.
  </p>
  
  <h2 class="page-header text-muted">
    输出
  </h2>
  
  <div class="content">
    Print the reversed sequence in a line. Print a single space character between adjacent elements (Note that your program should not put a space character after the last element).
  </div>
  
  <blockquote>
    <div>
      <p>
        n ≤ 100 ; 0 ≤ ai < 1000
      </p>
    </div>
  </blockquote>
  
  <div>
    <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,i;
    cin&gt;&gt;n;
    int a[100];
    for(i=0;i&lt;n;i++){
        scanf("%d",&a[i]);
    }
    for(i=n-1;i&gt;=0;i--){
        printf("%d ",a[i]);}
    return 0;
}</pre>
    
    <p>
      &nbsp;
    </p>
  </div>
</div>
