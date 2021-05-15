# 再解炸弹人

## 题目描述 {.page-header.text-muted}

<div class="content">
  现在炸弹不是想放在那里就能放在那里的了，必须由小人能够走到的地方才能放置炸弹。比如下面这个例子小人默认站在(3,3)这个位置。请问放在何处最多可以消灭多个敌人。<br /> <img loading="lazy" id="aimg_m7uLX" class="zoom" src="https://i0.wp.com/bbs.tianchai.org/data/attachment/forum/201312/30/211614zf17e3pvsjd3vf5e.png.thumb.jpg?resize=300%2C300" alt="" width="300" height="300" border="0" data-recalc-dims="1" />
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行4个整数为n m x y，分别n和m表示迷宫的行和列，x和y表示小人的起始坐标（从0行0列开始计算），接下来的n行m列为地图。 1<=n,m<=50
</div>

## 输出 {.page-header.text-muted}

最多可以消灭的敌人数。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
#define pi 3.14
#define mod 100
using namespace std;
typedef pair&lt;int,int&gt; Node;
typedef long long LL;
const int Max_n=55;
int n,m,sx,sy;
char a[Max_n][Max_n];
int vis[Max_n][Max_n],net[4][2]={{0,1},{1,0},{0,-1},{-1,0}};
int GetSum(int i,int j){
    int sum=0,x,y;
    x=i,y=j;
    while(a[x][y]!='#'){
        if(a[x][y]=='G')
            sum++;
            x--;
    }
    
    x=i,y=j;
    while(a[x][y]!='#'){
        if(a[x][y]=='G')
            sum++;
            x++; 
    }
    
    x=i,y=j;
    while(a[x][y]!='#'){ 
        if(a[x][y]=='G')
            sum++;
        y--; 
    }
    x=i,y=j;
    while(a[x][y]!='#'){
        if(a[x][y]=='G')
            sum++;
        y++; 
    }
    return sum;
}
 
int bfs(){
    memset(vis,0,sizeof(int));
    queue&lt;Node&gt;q;
    q.push(Node(sx,sy));
    vis[sx][sy]=1;
    int sum=0,mmax=0;
    while(q.size()){
        Node node=q.front();q.pop();
        sum=GetSum(node.first,node.second);
        if(sum&gt;mmax)
            mmax=sum;
        for(int i=0;i&lt;4;i++){
            int nx=node.first+net[i][0];
            int ny=node.second+net[i][1];
            if(nx&lt;0||nx&gt;=n||ny&lt;0||ny&gt;=m) continue;
            if(a[nx][ny]=='.'&&vis[nx][ny]==0){
                vis[nx][ny]=1;
                q.push(Node(nx,ny));
            }
        }
    }
    return mmax;
}
int main(){ 
    scanf("%d%d%d%d",&n,&m,&sx,&sy);
    for(int i=0;i&lt;n;i++)
        scanf("%s",a[i]);
    int mmax=bfs();
    printf("%d\n",mmax);
    return 0;
}</pre>

&nbsp;
