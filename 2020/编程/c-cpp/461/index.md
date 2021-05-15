# 统计字母个数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    给定一段文章，请输出每个字母出现的次数
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    只有一组输入数据，文件少于1000行。在文章中除最后一个字符外，只有大小写字母、空格和换行符，没有另外的标点、数字。该文章以’#’结尾。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出格式为“C A”，C为’a’..’z’中的字母，A为出现次数，C和A之间空一格
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    char r[1000],s[1000],c;
    int a[1000];
    int n,i,j,t=0;
    for(i='a',j=0; i&lt;='z'; i++)
      {
        a[j]=0;
        s[j++]=i;
      }
    int flag=1;
    while(flag!=0&&gets(r)){
    for(j=0; j&lt;strlen(r); j++)
    {
 
        if(r[j]=='#')
             {
            flag=0;
             break;
             }
        for(i=0; i&lt;26; i++)
        {
 
            if(s[i]==r[j]||(r[j]+32)==s[i])
                a[i]++;
        }
    }
    }
    for(i=0; i&lt;26; i++)
    {
        cout&lt;&lt;s[i]&lt;&lt;" "&lt;&lt;a[i]&lt;&lt;endl;
    }
 
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
