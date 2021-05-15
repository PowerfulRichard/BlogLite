# 通过年月判断天数

使用最简单的if语句实现给定年月判断天数

<pre class="EnlighterJSRAW" data-enlighter-language="cpp" data-enlighter-theme="godzilla">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
	int y, m, d;
	cin &gt;&gt; y &gt;&gt; m;
	if (y % 4 == 0 && y % 100 != 0 || y % 100 == 0 && y % 400 == 0) {
		if (m == 1 || m == 3) { d = 31; }
		if (m == 5 || m == 7) { d = 31; }
		if (m == 8 || m == 10) { d = 31; }
		if (m == 12) { d = 31; }
		if (m == 4 || m == 6) { d = 30; }
		if (m == 9 || m == 11) { d = 30; }
		if (m == 2) { d = 29; }
	}
	else {
		if (m == 1 || m == 3) { d = 31; }
		if (m == 5 || m == 7) { d = 31; }
		if (m == 8 || m == 10) { d = 31; }
		if (m == 12) { d = 31; }
		if (m == 4 || m == 6) { d = 30; }
		if (m == 9 || m == 11) { d = 30; }
		if (m == 2) { d = 28; }
		}
	cout &lt;&lt; d &lt;&lt; endl;
	return 0;
}</pre>

&nbsp;
