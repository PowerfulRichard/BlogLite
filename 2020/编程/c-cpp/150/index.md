# Swapping Two Numbers

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Swapping Two Numbers
  </p>
  
  <p>
    Write a program which reads two integers x and y, and prints them in ascending order.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input consists of multiple datasets. Each dataset consists of two integers x and y separated by a single space.
  </p>
  
  <p>
    The input ends with two 0 (when both x and y are zero). Your program should not process for these terminal symbols.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  For each dataset, print x and y in ascending order in a line. Put a single space between x and y.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
	int a,b;
	while(scanf("%d %d",&a,&b)!=EOF){
	    if(a==0&&b==0){
	        return 0;
	    }
	    else{
	        if(a&lt;b){
	            cout&lt;&lt;a&lt;&lt;" "&lt;&lt;b&lt;&lt;endl;
	        }
	        else{
	            cout&lt;&lt;b&lt;&lt;" "&lt;&lt;a&lt;&lt;endl;
	        }
	    }
	}
}</pre>

&nbsp;
