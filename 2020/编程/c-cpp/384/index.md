# 整数排序模板

将n换成求的位数

> 3位数比大小就是  n=3;  以此类推
> 
> 升序 降序只留一个

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n=3;                    //求几个数n就等于几 
    int a[n];
    int i,j,t;
    for(i=0; i&lt;n; i++){
        cin&gt;&gt;a[i];}
    sort(a,a+n);                        //升序 
    sort(a,a+n,greater&lt;int&gt;());           //降序 
    for(i=0; i&lt;n; i++){
        cout&lt;&lt;a[i]&lt;&lt;' ';}
        return 0;
}</pre>
