# 蟠桃记

算法一：求从后往前每次增加蟠桃数的通项公式，再累加

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
	int n,i=1,s=3,t=1;
	while(scanf("%d",&n)!=EOF){
		while(n&gt;i){
			i=i+1;
			t=t+s;
			s=2*s;
		}
		cout&lt;&lt;t&lt;&lt;endl;
		i=1;s=3;t=1;
	}
	return 0;
}</pre>

&nbsp;
