# Structured Program I – Print a Frame

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Print a Frame
  </p>
  
  <p>
    Draw a frame which has a height of H cm and a width of W cm. For example, the following figure shows a frame which has a height of 6 cm and a width of 10 cm.
  </p>
  
  <pre>##########
#........#
#........#
#........#
#........#
##########</pre>
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
    For each dataset, print the frame made of &#8216;#&#8217; and &#8216;.&#8217;.
  </p>
  
  <p>
    Print a blank line after each dataset.
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int a,b;
    while(scanf("%d %d",&a,&b)!=EOF)
    {
        if(a==0&&b==0)
        break;
        for(int i=1;i&lt;=a;i++)
        {
            if(i==1||i==a)
            {
            for(int j=0;j&lt;b;j++)
            {
                cout&lt;&lt;"#";
            }
            cout&lt;&lt;endl;
            }
            else
            {
                for(int j=1;j&lt;=b;j++)
                {
                    if(j==1||j==b)
                    cout&lt;&lt;"#";
                    else
                    cout&lt;&lt;"."; 
                }
                cout&lt;&lt;endl;
            }       
        }
        cout&lt;&lt;endl;
    } 
    return 0;       
}</pre>

&nbsp;
