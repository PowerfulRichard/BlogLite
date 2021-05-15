# 杨辉三角

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    按要求输入如下格式的杨辉三角
  </p>
  
  <p>
    1<br /> 1 1<br /> 1 2 1<br /> 1 3 3 1<br /> 1 4 6 4 1<br /> 1 5 10 10 5 1
  </p>
  
  <p>
    最多输出10层
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入只包含一个正整数n，表示将要输出的杨辉三角的层数。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对应于该输入，请输出相应层数的杨辉三角，每一层的整数之间用一个空格隔开
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int i,j,n,a[10][10];
    cin&gt;&gt;n;
    for(int t=0;t&lt;n;t++){
        a[t][0]=1;a[t][t]=1;
    }
    for(i=2;i&lt;n;i++){
        for(j=1;j&lt;i;j++){
            a[i][j]=a[i-1][j]+a[i-1][j-1];
        }
    }
    for(i=0;i&lt;n;i++){
        for(j=0;j&lt;=i;j++){
            cout&lt;&lt;a[i][j]&lt;&lt;" ";
        }
        cout&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
