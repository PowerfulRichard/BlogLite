# 未完成

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n,a[20][20],i,j,k,p,t;
    cin&gt;&gt;n;
    t=2*n+1;
    for(k=n; k&gt;=0; k=k-1) {
        for(i=1;i&lt;t;i++){
            for(j=1;j&lt;t;j++){
                a[i][j]=k;
            }
        }t=t-1;
    }
    for(i=1;i&lt;2*n+1;i++){
        for(j=1;j&lt;2*n+1;j++){
            cout&lt;&lt;setw(2)&lt;&lt;a[i][j];
        }cout&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
