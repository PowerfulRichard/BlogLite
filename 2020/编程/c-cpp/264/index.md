# 打印星星三角形

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    打印如下的三角形（n=3）
  </p>
  
  <p>
    *
  </p>
  
  <p>
    **
  </p>
  
  <p>
    ***
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  三角形的层数n
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  打印好的三角形
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,i,j;
    cin&gt;&gt;n;
    for(i=0;i&lt;n;i++)
    {
        for(j=0;j&lt;=i;j++)
            printf("*");
        printf("\n");
    }
    printf("\n");
    return 0;
}</pre>

&nbsp;
