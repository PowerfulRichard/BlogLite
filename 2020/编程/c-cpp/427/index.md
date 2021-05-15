# 做幻方

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Apple最近迷上了做幻方，Apple还是个中高手，只要你说个奇数N就能把N*N的幻方做出来。其实你可以比他做得更好的。Apple总是画得很乱，而你可以利用程序排得很整齐^_^ 幻方的要求：每一行，每一列，还有两条斜线上数字的和都相等.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    每行一个奇数N(0< N < 30),输入0结束
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输入一个奇数，输出一个幻方，顺序参照样板输出；数与数用一个空格分开；输出完以后加一个回车。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int a[100][100];
int n;
void show() {
    for (int i = 0; i &lt; n; i++) {
        for (int j = 0; j &lt; n; j++) {
            cout &lt;&lt; a[i][j] &lt;&lt; " ";
        }
        cout &lt;&lt; endl;
    }
}
void cal() {
    memset(a, 0, sizeof(a));
    int x = n - 1, y = n / 2;
    a[x][y] = 1;
    for (int k = 2; k &lt;= n * n; k++) {
        int nx = (x + 1) % n;
        int ny = (y + 1) % n;
        if (a[nx][ny] != 0) {
            nx = (x - 1 + n) % n;
            ny = y;
        }
        a[nx][ny] = k;
        x = nx;
        y = ny;
    }
}
int main() {
    while (cin &gt;&gt; n) {
        cal();
        show();
        cout &lt;&lt; endl;
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
