# 最长单词（输出最长字符串）

## 题目描述 {.page-header.text-muted}

<div class="content">
  编写一个函数，输入一行字符，将此字符串中最长的单词输出。<br /> 输入仅一行，多个单词，每个单词间用一个空格隔开。单词仅由小写字母组成。所有单词的长度和不超过100000。如有多个最长单词，输出最先出现的。
</div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    char a[100000],b[100000];
    int aa,bb;
    scanf("%s",&a);
    strcpy(b,a);
    while(scanf("%s",&a)!=EOF){
        aa=strlen(a);bb=strlen(b);
        if(aa&gt;bb){
            strcpy(b,a);
        }
    }
    printf("%s",b);
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
