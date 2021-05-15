# 水池数目

## 题目描述 {.page-header.text-muted}

<div class="content">
  安徽科技学院校园里有一些小河和一些湖泊，现在，我们把它们通一看成水池，假设有一张我们学校的某处的地图，这个地图上仅标识了此处是否是水池，现在，你的任务来了，请用计算机算出该地图中共有几个水池。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行输入一个整数N，表示共有N组测试数据<br /> 每一组数据都是先输入该地图的行数n(0<n<100)与列数m(0<m<100)，然后，输入接下来的m行每行输入n个数，表示此处有水还是没水（1表示此处是水池，0表示此处是地面）
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出该地图中水池的个数。<br /> 要注意，每个水池的旁边（上下左右四个位置）如果还是水池的话的话，它们可以看做是同一个水池。</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
#define MAXN 105
int dx[4]={0,-1,0,1};
int dy[4]={-1,0,1,0};
int mapp[MAXN][MAXN];
int m,n;
void dfs(int x,int y){
    mapp[x][y]=-1;
    for(int i=0;i&lt;4;i++){
        int nx=x+dx[i];
        int ny=y+dy[i];
        if(nx&gt;=0 && nx&lt;m && ny&gt;=0 && ny&lt;=n && mapp[nx][ny]==1){
            mapp[nx][ny]==-1;
            dfs(nx,ny);
        }
    }
}
int main(){
    int T;
    scanf("%d\n",&T);
    while(T--){
        int ans=0;
        scanf("%d%d",&m,&n);
        for(int i=0;i&lt;m;i++){
            for(int j=0;j&lt;n;j++){
                scanf("%d",&mapp[i][j]);
            }
        }
        for(int i=0;i&lt;m;i++){
            for(int j=0;j&lt;n;j++){
                if(mapp[i][j]==1){
                    dfs(i,j);
                    ans++;
                }
            }
        }
        printf("%d\n",ans);
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
