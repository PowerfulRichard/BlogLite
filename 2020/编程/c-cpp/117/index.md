# 四位数排序

算法：和三位数排序相同，在三位数的基础上多一个与数字d的比较

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a, b, c, d;
    int x;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    if (a &lt; b)
    {
        x = a; a = b; b = x;
    }
    if (a &lt; c)
    {
        x = a; a = c; c = x;
    }
    if (a &lt; d)
    {
        x = a; a = d; d = x;
    }
    if (b &lt; c) {
        x = b; b = c; c = x;
    }
    if (b &lt; d) {
        x = b; b = d; d = x;
    }
    if (c &lt; d) {
        x = c; c = d; d = x;
    }
    printf("%d %d %d %d", d, c, b, a);
    return 0;
}</pre>

数组法

> c++中有求最大值函数

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a[4],i;
    for(i=0;i&lt;4;i++){
        cin&gt;&gt;a[i];
    }
    cout&lt;&lt;(*max_element(a, a+ 4));
}</pre>

&nbsp;
