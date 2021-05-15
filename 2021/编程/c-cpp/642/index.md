# 孪生素数

## 题目描述 {.page-header.text-muted}

<div class="content">
  在质数的大家庭中，大小之差不超过2的两个质数称它俩为一对孪生素数，如2和3、3和5、17和19等等。请你统计一下，在不大于自然数N的质数中，孪生素数的对数。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  只有一行，一个自然数N。(N<=10^6)
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  只有一行，一个整数，表示N以内孪生素数的对数。</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int is(int num) {
    for (int i = 2; i &lt;= sqrt((double)num); ++i)if (num % i == 0)return 0;
    return 1;
}
int main() {
    int n, count = 0, len = -1;
    scanf("%d", &n);
    int arr[100000] = { 0 };
    for (int i = 2; i &lt;= n; ++i) {
        if (is(i))arr[++len] = i;
    }
    for (int i = 0; i &lt; len; ++i) {
        if (arr[i + 1] - arr[i] &lt;= 2)
            count++;
    }
    printf("%d", count);
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
