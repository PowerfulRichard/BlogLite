# 

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int f(int t){
    if(t&lt;4)return 1;
    return f(t-3)+f(t-1);
}
int main(){
    int n;
    cin&gt;&gt;n;
    cout&lt;&lt;f(n)&lt;&lt;endl;
    return 0;
}</pre>

&nbsp;
