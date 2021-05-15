# 给定秒数计算小时分钟（时间转换）

<div class="content">
  <h2 class="page-header text-muted">
    题目描述
  </h2>
  
  <div class="content">
    给定一个以秒为单位的时间t，要求用  “< H> :< M> :< S> ”的格式来表示这个时间。< H> 表示时间，< M> 表示分钟，  而< S> 表示秒，它们都是整数且没有前导的“0”。例如，若t=0，则应输出是“0:0:0”；若t=3661，则输出“1:1:1”。
  </div>
  
  <h2 class="page-header text-muted">
    输入
  </h2>
  
  <div class="content">
    输入只有一行，是一个整数t（0< =t< =86399）。
  </div>
  
  <h2 class="page-header text-muted">
    输出
  </h2>
  
  <div class="content">
    输出只有一行，是以“< H> :< M> :< S> ”的格式所表示的时间，不包括引号。
  </div>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp" data-enlighter-theme="godzilla">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int h, m,s,x;
    scanf("%d",&x);
    h=x/3600;
    m=(x-(h*3600))/60;
    s=(x-(h*3600)-m*60);
    cout&lt;&lt;h&lt;&lt;":"&lt;&lt;m&lt;&lt;":"&lt;&lt;s;
    return 0;
}</pre>

&nbsp;
