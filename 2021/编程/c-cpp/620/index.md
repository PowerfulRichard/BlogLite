# 查找最大元素

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">对于输入的每个字符串，查找其中的最大字母，在该字母后面插入字符串“(max)”。</span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">输入数据包括多个测试实例，每个实例由一行长度不超过100的字符串组成，字符串仅由大小写字母及数字构成</span>
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">对于每个测试实例输出一行字符串，输出的结果是插入字符串“(max)”后的结果，如果存在多个最大的字母，就在每一个最大字母后面都插入&#8221;(max)&#8221;。</span>
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    char a[100];
    int len;
    int b[100];
    char max;
    while(cin&gt;&gt;a)
    {       
        len=strlen(a);
        max=a[0];
        for(int i=0;i&lt;len;i++)
        {           
            if(max&lt;a[i])
            {
                max=a[i];
                        
            }
        }
        
        for(int i=0;i&lt;len;i++)
        {
            cout&lt;&lt;a[i];
            if(a[i]==max)
            {
                cout&lt;&lt;"(max)";    
            }
            
        }
        cout&lt;&lt;endl;
        
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
