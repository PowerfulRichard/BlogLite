# 子序列之和

## 题目描述 {.page-header.text-muted}

<div class="content">
  给定两个整数n m, 0 < n < m < 10^6 输出1/n^2+1/(n+1)^2+&#8230;.+1/m^2保留5位小数，例如n=2 m=4 答案是0.42361 n=65536 m=655360 答案是0.00001.
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  有多组测试数据，每一行有n m
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  1/n^2+1/(n+1)^2+&#8230;.+1/m^2保留5位小数
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
	int n,m;
	long double s=0;
	while(scanf("%d %d",&n,&m)!=EOF){
	    while(n&lt;=m){
	        long double nn=(int)n;
	        s=s+(1/(nn*nn));
	        n=n+1;
	    }
	    printf("%.5Lf\n",s);
	    s=0;
	}
	return 0;
}</pre>

&nbsp;
