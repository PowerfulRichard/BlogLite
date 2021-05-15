# 水仙花问题（3）

判断多组数据是否为水仙花数

算法：使用while多次读取数值，并计算是否为水仙花数

<pre class="EnlighterJSRAW" data-enlighter-language="c">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
int main() {
	int x, a, b, c;
	while (scanf("%d", &x) != EOF) {
		if (x == 0) {
			return 0;
		}
		a = x % 10;
		b = ((x % 100) - a) / 10;
		c = (((x % 1000) - a) - 10 * b) / 100;
		if (x == (a * a * a) + (b * b * b) + (c * c * c)) {
			printf("Yes\n");
		}
		else {
			printf("No\n");
		}
	}
}</pre>

&nbsp;
