# 扫雷

## 题目描述 {.page-header.text-muted}

<div class="content">
  扫雷是一个经典的游戏，在一个N*M区域中<br /> 输入一个N*M的雷区中的k个雷坐标，打印出所有雷区的分布<br /> 一个位置如果是雷则表示为*,否则应该是0~8，表示他周围八连通域中的地雷总数。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  雷区尺寸 3=<n m=&#8221;&#8221; <=&#8221;20&#8243;<br /> 地雷数目 k<=M*N<br /> 和他们的坐标xi,yi
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  雷区的分布<br /> 每组后空一行
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
const int maxn = 21;
const int BOMB = 999;
int a[maxn][maxn];
int m, n, k, x, y;
void show() {
    for (int i = 0; i &lt; n; i++) {
        for (int j = 0; j &lt; m; j++) {
            if (a[i][j] != BOMB) {
                cout &lt;&lt; a[i][j];
            }
            else {
                cout &lt;&lt; "*";
            }
        }
        cout &lt;&lt; endl;
    }
}
void cal() {
    for (x = 0; x &lt; n; x++) for (y = 0; y &lt; m; y++) {
        if (a[x][y] == BOMB) {
            continue;
        }
        int& tot = a[x][y];
        for (int dx = -1; dx &lt;= 1; ++dx) for (int dy = -1; dy &lt;= 1; ++dy) {
            if (dx == 0 && dy == 0) {
                continue;
            }
            int nx = x + dx;
            int ny = y + dy;
            if (nx &lt; 0 || nx &gt;= n || ny &lt; 0 || ny &gt;= m) {
                continue;
            }
            if (a[nx][ny] == BOMB) {
                ++tot;
            }
        }
    }
}
void input() {
    memset(a, 0, sizeof(a));
    while (k--) {
        cin &gt;&gt; x &gt;&gt; y;
        a[x][y] = BOMB;
    }
}
int main() {
    while (cin &gt;&gt; n &gt;&gt; m &gt;&gt; k) {
        input();
        cal();
        show();
        cout &lt;&lt; endl;
    }
    return 0;
}
</pre>

&nbsp;
