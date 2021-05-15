# Structured Program I – Print a Rectangle

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Print a Rectangle
  </p>
  
  <p>
    Draw a rectangle which has a height of H cm and a width of W cm. Draw a 1-cm square by single &#8216;#&#8217;.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input consists of multiple datasets. Each dataset consists of two integers H and W separated by a single space.
  </p>
  
  <p>
    The input ends with two 0 (when both H and W are zero).
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    For each dataset, print the rectangle made of H × W &#8216;#&#8217;.
  </p>
  
  <p>
    Print a blank line after each dataset.
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int h,w,i,j;
    while(scanf("%d %d",&h,&w)!=EOF)
    {
        if(h==0&&w==0){
            return 0;
        }
        else {
            for(i=0;i&lt;h;i=i+1){
                for(j=0;j&lt;w;j=j+1){
                    cout&lt;&lt;"#";
                }
                cout&lt;&lt;endl;
            }
            printf("\n");}
    }
}</pre>

&nbsp;
