# 明明的随机数

## 题目描述 {.page-header.text-muted}

<div class="content">
  明明想在学校中请一些同学一起做一项问卷调查，为了实验的客观性，他先用计算机生成了N个1到1000之间的随机整数（N≤100），对于其中重复的数字，只保留一个，把其余相同的数去掉，不同的数对应着不同的学生的学号。然后再把这些数从小到大排序，按照排好的顺序去找同学做调查。请你协助明明完成“去重”与“排序”的工作。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <pre>输入有2行
第1行为1个正整数，表示所生成的随机数的个数：N
第2行有N个用空格隔开的正整数，为所产生的随机数。</pre>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <pre>输出也是2行，第1行为1个正整数M，表示不相同的随机数的个数。第2行为M个用空格隔开的正整数，为从小到大排好序的不相同的随机数。</pre>
</div>

_常规解法_

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
using namespace std;
int main(){
    int N,n;
    int a[1000];
    int i,j,k;
    while(scanf("%d",&n)!=EOF){
        for(i=0; i&lt;n; i++)
            scanf("%d",&a[i]);
        //去重
        for(i=0; i&lt;n; i++)
            for(j=i+1; j&lt;n; j++){
                if(a[j]==a[i]){
                    for(k=j; k&lt;n-1; k++)
                        a[k]=a[k+1];
                    n--;
                    j--;
                }
            }
        //冒泡排序
        for(i=0; i&lt;n-1; i++)
            for(j=0; j&lt;n-1-i; j++){
                if(a[j]&gt;a[j+1]){
                    int temp=a[j];
                    a[j]=a[j+1];
                    a[j+1]=temp;
                }
            
            }
        for(i=0; i&lt;n; i++){
            cout&lt;&lt;a[i]&lt;&lt;endl;
        }
    }
}</pre>

_奇技淫巧_

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n, a[101], i;
    cin &gt;&gt; n;
    for (i = 0; i &lt; n; i++) { cin &gt;&gt; a[i]; }
    sort(a, a + n);
    int t = unique(a, a + n) - a;
    cout &lt;&lt; t &lt;&lt; endl;
    for (i = 0; i &lt; t; i++) { cout &lt;&lt; a[i] &lt;&lt; " "; }
}</pre>

_网传大佬解法_

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int n,k,i,a[1001],x;
int main()
{
    cin&gt;&gt;n;
    memset(a,0,sizeof(a));
    for(i=1;i&lt;=n;i++)
   {
        cin&gt;&gt;x;
        if(a[x]==0) k++;
        a[x]++;
   }
    cout&lt;&lt;k&lt;&lt;endl;
   for(int i=1;i&lt;=1000;i++)
        if(a[i]&gt;0) cout&lt;&lt;i&lt;&lt;" ";
   return 0;
}</pre>

&nbsp;
