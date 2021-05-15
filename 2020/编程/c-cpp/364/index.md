# 斜率计算

## 题目描述 {.page-header.text-muted}

<div class="content">
  输入两个点的坐标，即p1  =  (x1,  y1)和p2=(x2,  y2)，求过这两个点的直线的斜率。如果斜率为无穷大输出“INF”。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int slope(int x1,int y1,int x2,int y2){
    return (y2-y1)/(x2-x1);
}
int main(){
    int x1,y1,x2,y2,t;
    while(scanf("%d %d %d %d",&x1,&y1,&x2,&y2)!=EOF){
        if(x1==x2){
            cout&lt;&lt;"INF"&lt;&lt;endl;continue;
        }
        if(y1==y2){
            cout&lt;&lt;"0"&lt;&lt;endl;continue;
        }
        cout&lt;&lt;slope(x1,y1,x2,y2)&lt;&lt;endl;
    }
    
    return 0;
}</pre>

&nbsp;
