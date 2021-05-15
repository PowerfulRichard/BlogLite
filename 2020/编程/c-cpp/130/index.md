# Repetitive Processing – Print Test Cases

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Print Test Cases
  </p>
  
  <p>
    In an online judge system, a judge file may includes multiple datasets to check whether the submitted program outputs a correct answer for each test case. This task is to practice solving a problem with multiple datasets.
  </p>
  
  <p>
    Write a program which reads an integer x and print it as is. Note that multiple datasets are given for this problem.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input consists of multiple datasets. Each dataset consists of an integer x in a line.
  </p>
  
  <p>
    The input ends with an integer 0. You program should not process (print) for this terminal symbol.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    For each dataset, print x in the following format:
  </p>
  
  <p>
    Case i: x
  </p>
  
  <p>
    where i is the case number which starts with 1. Put a single space between &#8220;Case&#8221; and i. Also, put a single space between &#8216;:&#8217; and x.
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,i=0;
	while(scanf("%d",&a)!=EOF){
		if(a==0){
			return 0;
		}
		else{
	    i=i+1;
	    printf("Case %d: %d\n",i,a);
	    a=0;}
	}
	
	return 0;
}</pre>

&nbsp;
