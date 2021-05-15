# 鸡兔同笼

## 题目描述 {.page-header.text-muted}

<div class="content">
  已知鸡和兔的总数量为n,总腿数为m。输入n和m,依次输出鸡和兔的数目，如果无解，则输出“No answer”(不要引号)。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    第一行输入一个数据a,代表接下来共有几组数据，在接下来的(a<10)<br /> a行里，每行都有一个n和m. (1<=n,m<=1000)
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出鸡兔的个数，或者No answer
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,n,m,x,y;
    cin&gt;&gt;a;
    while(a--){
        cin&gt;&gt;n&gt;&gt;m;
        if(m%2==0){
            y=(m-2*n)/2; //tu
            x=n-y; //ji
            if(x&gt;=0&&y&gt;=0){
                cout&lt;&lt;x&lt;&lt;" "&lt;&lt;y&lt;&lt;endl;
            }
            else{
                cout&lt;&lt;"No answer"&lt;&lt;endl;
            }
        }
        else{
            cout&lt;&lt;"No answer"&lt;&lt;endl;
        }
    }

    return 0;
}</pre>

&nbsp;
