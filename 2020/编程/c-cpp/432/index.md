# 螺旋矩阵

## 题目描述 {.page-header.text-muted}

<div class="content">
  给定一个正整数n(１＜＝ｎ＜＝２０)，画出螺旋矩阵。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    一个正整数n
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    对应画出螺旋矩阵
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
const int maxn = 21;
int a[maxn][maxn];
int n;
void show() {
    for (int x = 0; x &lt; n; x++) {
        for (int y = 0; y &lt; n; y++) {
            cout &lt;&lt; a[x][y] &lt;&lt; " ";
        }
        cout &lt;&lt; endl;
    }
}
void cal() {
    int x = 0, y = 0;
    a[x][y] = 1;
    for (int k = 2; k &lt;= n * n; ) {
        while (1) {
            int nx = x, ny = y + 1;
            if (nx &lt; 0 || nx &gt;= n || ny &lt; 0 || ny &gt;= n || a[nx][ny]) {
                break;
            }
            a[x = nx][y = ny] = k++;
        }
        while (1) {
            int nx = x + 1, ny = y;
            if (nx &lt; 0 || nx &gt;= n || ny &lt; 0 || ny &gt;= n || a[nx][ny]) {
                break;
            }
            a[x = nx][y = ny] = k++;
        }
        while (1) {
            int nx = x, ny = y - 1;
            if (nx &lt; 0 || nx &gt;= n || ny &lt; 0 || ny &gt;= n || a[nx][ny]) {
                break;
            }
            a[x = nx][y = ny] = k++;
        }
        while (1) {
            int nx = x - 1, ny = y;
            if (nx &lt; 0 || nx &gt;= n || ny &lt; 0 || ny &gt;= n || a[nx][ny]) {
                break;
            }
            a[x = nx][y = ny] = k++;
        }
    }
}
int main() {
    cin &gt;&gt; n;
    cal();
    show();
    return 0;
}</pre>

&nbsp;
