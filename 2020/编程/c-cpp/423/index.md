# 回形方阵

## 题目描述 {.page-header.text-muted}

<div class="content">
  输出一个回形方阵，具体可见样例
</div>

### 输入 {.page-header.text-muted}

<div class="content">
  一个整数n （0 ＜ n ＜ 10）
</div>

### 输出 {.page-header.text-muted}

<div class="content">
  <p>
    一个方阵，每个数字的定宽为2
  </p>
  
  <h3>
    提示
  </h3>
  
  <p>
    实现定宽为2：C语言用<code>printf("%2d",x);</code>   C++用<code>cout&lt;&lt;setw(2)&lt;&lt;x;</code>
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;bits/stdc++.h&gt;
using namespace std;
int a[100][100];
int n, size;
void input() {
    cin &gt;&gt; n;
}
void cal() {
    size = 2 * n + 1;
    for (int j = 0; j &lt; size; j++) {
        for (int i = 0; i &lt; size; i++) {
            a[i][j] = max(abs(i - n), abs(j - n));
        }
    }
}
void show() {
    for (int i = 0; i &lt; size; i++) {
        for (int j = 0; j &lt; size; j++) {
            cout &lt;&lt; " " &lt;&lt; a[i][j];
        }
        cout &lt;&lt; endl;
    }
}
int main() {
    input();
    cal();
    show();
    return 0;
}
</pre>
  
  <p>
    &nbsp;
  </p>
</div>
