# 数字三角形

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span class="Apple-style-span">7<span class="Apple-converted-space"> </span><br /> 3 8<span class="Apple-converted-space"> </span><br /> 8 1 0<br /> 2 7 4 4<br /> 4 5 2 6 5<span class="Apple-converted-space"> </span><br /> (图一)<span class="Apple-converted-space"> </span><br /> 图一表示一个5行的数字三角形。假设给定一个n行数字三角形,计算出从三角形顶至底的一条路径，使该路径经过的数字总和最大。<span class="Apple-converted-space"> </span><br /> 每一步只能由当前位置向下或向右下。<br /> </span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span class="Apple-style-span">你的程序要能接受标准输入。第一行包含一个整数T，表示总的测试次数。<span class="Apple-converted-space"> </span><br /> 对于每一种情况：第一行包含一个整数N,其中1 < N < 100,表示三角形的行数。<span class="Apple-converted-space"> </span><br /> 接下来的N行输入表示三角形的每一行的元素Ai,j，其中0 < Ai,j < 100。</span>
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    <span class="Apple-style-span">输出每次测试的最大值并且占一行。</span>
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int n, i, j, a[110][110] = { 0 };
    int t;
    scanf("%d", &t);
    while (t--) {
        scanf("%d\n", &n);
        for (i = 0; i &lt;= n - 1; i++) {
            for (j = 0; j &lt;= i; j++) {
                scanf("%d\n", &a[i][j]);
            }
        }
        for (i = n - 2; i &gt;= 0; i--) {
            for (j = 0; j &lt;= i; j++) {
                a[i][j] = a[i][j] + max(a[i + 1][j], a[i + 1][j + 1]);
            }
        }
        printf("%d\n", a[0][0]);
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
