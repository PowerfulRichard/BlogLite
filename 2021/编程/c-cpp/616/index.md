# 雄伟的城堡

<h2 style="font-weight: 500;">
  题目描述
</h2>

在一个群岛上，有一个富可敌国的大富翁。他打算在这个群岛上建造一个最大城堡，也就是群岛上最大的岛屿。

<h2 style="font-weight: 500;">
  输入
</h2>

第一行是一个整数T，代表测试数据的组数。每组数据中第一行是两个整数n,m，代表地图的大小。接下来n行每行共m个整数。0代表海洋，1代表陆地。其中T<=50,n,m<=200

<h2 style="font-weight: 500;">
  输出
</h2>

共T行，最大的面积。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;bits/stdc++.h&gt;
using namespace std;
#define MAXN 205
int n, m;
bool G[MAXN][MAXN];
int idx[MAXN][MAXN];
int iMax;
void dfs(int r, int c, int id, int &cnt) {
    if(r&lt;0 || r&gt;=n || c&lt;0 || c&gt;=m) return;
    if(G[r][c]==0 || idx[r][c]&gt;0) return;
    idx[r][c] = id;
    cnt++;
    dfs(r-1, c, id, cnt);
    dfs(r, c+1, id, cnt);
    dfs(r+1, c, id, cnt);
    dfs(r, c-1, id, cnt);
}
void doo() {
    memset(G, 0, sizeof(G));
    memset(idx, 0, sizeof(idx));
    iMax = 0;
    cin &gt;&gt; n &gt;&gt; m;
    for(int i=0; i&lt;n; i++)
        for(int j=0; j&lt;m; j++)
            cin &gt;&gt; G[i][j];
    int id = 0;
    for(int i=0; i&lt;n; i++)
        for(int j=0; j&lt;m; j++) {
            int cnt = 0;
            if(G[i][j]==1 && idx[i][j]==0) dfs(i, j, ++id, cnt);
            if(cnt &gt; iMax) iMax = cnt;
        }
   
    cout &lt;&lt; iMax &lt;&lt; endl;
}
int main()
{
   
    int T;
    cin &gt;&gt; T;
    while(T--)
        doo();
    return 0;
}</pre>

&nbsp;
