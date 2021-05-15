# Structured Program I – Print a Chessboard

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Print a Chessboard
  </p>
  
  <p>
    Draw a chessboard which has a height of H cm and a width of W cm. For example, the following figure shows a chessboard which has a height of 6 cm and a width of 10 cm.
  </p>
  
  <pre>#.#.#.#.#.
.#.#.#.#.#
#.#.#.#.#.
.#.#.#.#.#
#.#.#.#.#.
.#.#.#.#.#</pre>
  
  <p>
    Note that the top left corner should be drawn by &#8216;#&#8217;.
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
    For each dataset, print the chessboard made of &#8216;#&#8217; and &#8216;.&#8217;.
  </p>
  
  <p>
    Print a blank line after each dataset.
  </p>
</div>

## 解法一：

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
using namespace std;
int main()
{
    int h,w;
    cin &gt;&gt; h &gt;&gt; w;
    while(h!=0)
    {
        int i,j;
        for(i=0;i&lt;h;i++)
        {
            for(j=0;j&lt;w;j++)
            {
                if((i%2==0&&j%2==0||i%2==1&&j%2==1))
                cout &lt;&lt; "#";
                else cout &lt;&lt; ".";
            }
            cout &lt;&lt; endl;
        }
        cout &lt;&lt; endl;
        cin &gt;&gt; h &gt;&gt; w;
    }
    return 0;
}</pre>

## 解法二（有错误）：

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int h,w,i=0,j;
    while(scanf("%d %d",&h,&w)!=EOF) {
        if(h==0&&w==0) {
            break;
        } else {
            for(j=1; j&lt;=h; j++) {
                if(j%2!=0) {
                    for(i=1; i&lt;=w; i++) {
                        if(i%2==0) {
                            cout&lt;&lt;".";
                        } else {
                            cout&lt;&lt;"#";
                        }
                    }
                } else {
                    for(i=1; i&lt;=w; i++) {
                        if(i%2==0) {
                            cout&lt;&lt;"#";
                        } else {
                            cout&lt;&lt;".";
                        }
                    }
                }
                cout&lt;&lt;endl;
            }
        }
    }
    return 0;
}</pre>

&nbsp;
