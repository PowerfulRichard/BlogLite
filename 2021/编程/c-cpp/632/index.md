# 全排列

## 题目描述 {.page-header.text-muted}

<div class="content">
  输入一个自然数N（1<=N<=9），从小到大输出用1~N组成的所有排列，也就说全排列。例如输入3则输出<br /> 123<br /> 132<br /> 213<br /> 231<br /> 312<br /> 321
</div>

## 输入 {.page-header.text-muted}

输入一个自然数N（1<=N<=9）

## 输出 {.page-header.text-muted}

N的全排列，每行一个

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;bits/stdc++.h&gt;
using namespace std;
int n,flag[10],a[10];
void dfs(int s)
{
    if(s==n+1)
    {
        for(int i=1;i&lt;=n;i++)
            printf("%d",a[i]);
        printf("\n");
    }
    for(int i=1;i&lt;=n;i++)
    {
        if(flag[i]==0)
        {
            a[s]=i;
            flag[i]=1;
            dfs(s+1);
            flag[i]=0;
        }
    }
    return;
}
int main()
{
    scanf("%d",&n);
    dfs(1);
    return 0;
}</pre>

&nbsp;
