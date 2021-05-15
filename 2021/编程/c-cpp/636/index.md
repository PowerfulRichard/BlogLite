# 海上救援

## 题目描述 {.page-header.text-muted}

<div class="content">
  小L在坐尼克泰坦号去旅游的时候发生了意外，不慎掉入了大海里，现在需要擅长游泳的你去救他，可是他的身边被鲨鱼包围了，如果有空隙的话你可以趁鲨鱼不注意游过去救他，可如果鲨鱼将小L完全围住，那他就只能去见JACK了，现在请你判断你是否可以成功救出他。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  多组输入 第一行包含两个正整数<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">n</span></span></span></span>,<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">m</span></span> ,<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi><mo>&#x2264;</mo><mn>50</mn><mo>,</mo><mi>m</mi><mo>&#x2264;</mo><mn>50</mn></math>"><span id="MathJax-Span-23" class="math"><span id="MathJax-Span-24" class="mrow"><span id="MathJax-Span-25" class="mi">n</span><span id="MathJax-Span-26" class="mo">≤</span><span id="MathJax-Span-27" class="mn">50</span><span id="MathJax-Span-28" class="mo">,</span><span id="MathJax-Span-29" class="mi">m</span><span id="MathJax-Span-30" class="mo">≤</span><span id="MathJax-Span-31" class="mn">50,</span></span></span></span>表示大海的长度和宽度 第二行为<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi><mo>&#x00D7;</mo><mi>m</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">n×m</span></span>的矩阵，其中：*表示海水，x表示鲨鱼，<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>L</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">L</span></span>表示小L的位置，<span id="MathJax-Element-11-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>S</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">S</span></span>表示你的位置 （你只能朝上下左右四个方向移动）
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    如果能救出小L，输出：I saved him.
  </p>
  
  <p>
    否则输出：Sorry, I can&#8217;t save him.
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
const int maxn=999;
int n,m,flag;
char a[maxn][maxn];
int X[4]={0,0,1,-1};
int Y[4]={1,-1,0,0};
bool inq[maxn][maxn];
struct node{
    int x;
    int y;
}s,g,Node;
bool judge(int x,int y){
    if(x&lt;0||x&gt;=n||y&lt;0||y&gt;=m)return false;
    if(a[x][y]=='x'||inq[x][y]==true)return false;
    return true;
}
void bfs(){
    queue&lt;node&gt;q;
    q.push(s);
    while(q.empty()!=1){
        node top=q.front();
        q.pop();
        if(top.x==g.x&&top.y==g.y){
            flag=1;
            return;
        }
        for(int i=0;i&lt;4;i++){
            int newx=top.x+X[i];
            int newy=top.y+Y[i];
            if(judge(newx,newy)){
                Node.x=newx,Node.y=newy;
                q.push(Node);
                inq[newx][newy]=true;
            }
        }
    }
}
int main(){
    ios::sync_with_stdio(false);
    cin.tie(0);
    cout.tie(0);
    while(cin&gt;&gt;n&gt;&gt;m){
        flag=0;
        for(int i=0;i&lt;n;i++){
            for(int j=0;j&lt;m;j++){
                cin&gt;&gt;a[i][j];
                inq[i][j]=false;
            }
        }
        for(int i=0;i&lt;n;i++){
            for(int j=0;j&lt;m;j++){
                if(a[i][j]=='S'){
                    s.x=i,s.y=j;
                }else if(a[i][j]=='L'){
                    g.x=i,g.y=j;
                }
            }
        }
        bfs();
        if(flag==1)cout&lt;&lt;"I saved him."&lt;&lt;endl;
        else if(flag==0)cout&lt;&lt;"Sorry, I can't save him."&lt;&lt;endl;
    }
    
    return 0;
}
</pre>
  
  <p>
    &nbsp;
  </p>
</div>
