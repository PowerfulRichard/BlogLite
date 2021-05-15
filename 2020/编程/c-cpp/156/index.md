# Circle

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Circle
  </p>
  
  <p>
    Write a program which calculates the area and circumference of a circle for given radius r.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  A real number r is given.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Print the area and circumference of the circle in a line. Put a single space between them. The output should not contain an absolute error greater than 10^-5.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
#define pi 3.14159265358979323846264338327950288419716939937510
using namespace std;
int main(){
	long double r,s,c;
	scanf("%Lf",&r);
	c=2*pi*r;
	s=pi*r*r;
	printf("%Lf %Lf",s,c);
	return 0;
}</pre>

&nbsp;
