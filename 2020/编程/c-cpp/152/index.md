# A / B Problem

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    A/B Problem
  </p>
  
  <p>
    Write a program which reads two integers a and b, and calculates the following values:
  </p>
  
  <p>
    a ÷ b: d (in integer)
  </p>
  
  <p>
    remainder of a ÷ b: r (in integer)
  </p>
  
  <p>
    a ÷ b: f (in real number)
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  Two integers a and b are given in a line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Print d, r and f separated by a space in a line. For f, the output should not contain an absolute error greater than 10^-5.
</div>

> 注：此题为特殊判断机制（special judge），精确到小数点**后6位**（long double默认精确度）即可。

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    long double a,b;
	scanf("%Lf %Lf",&a,&b);
	int c=(int)a;
	int d=(int)b;
	printf("%d %d %Lf",c/d,c%d,a/b);
	return 0;
}</pre>

&nbsp;
