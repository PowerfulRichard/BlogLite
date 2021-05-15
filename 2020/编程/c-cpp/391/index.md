# 三个数求最大值

数组解法

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n[3],i;
    for(i=0;i&lt;3;i++){
        cin&gt;&gt;n[i];
    }
    cout&lt;&lt;(*max_element(n, n + 3));
}</pre>

&nbsp;
