# Simple Calculator

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Simple Calculator
  </p>
  
  <p>
    Write a program which reads two integers a, b and an operator op, and then prints the value of a op b.
  </p>
  
  <p>
    The operator op is &#8216;+&#8217;, &#8216;-&#8216;, &#8216;*&#8217; or &#8216;/&#8217; (sum, difference, product or quotient). The division should truncate any fractional part.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input consists of multiple datasets. Each dataset is given in the following format.
  </p>
  
  <p>
    a op b
  </p>
  
  <p>
    The input ends with a single &#8216;?&#8217;. Your program should not process for this terminal symbol.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  For each dataset, print the value in a line.
</div>

> <div>
>   重点就在于比较符号是否相等
> </div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
	int a,b,z,s;
	while(scanf("%d %c %d",&a,&z,&b)!=EOF){
	    if (z=='+'){
	        s=a+b;
	    }
	    if (z=='-'){
	        s=a-b;
	    }
	    if (z=='*'){
	        s=a*b;
	    }
	    if (z=='/'){
	        s=a/b;
	    }
	    if (z=='?'){
	        return 0;
	    }
	    cout&lt;&lt;s&lt;&lt;endl;
	    s=0;
	}
}</pre>

&nbsp;
