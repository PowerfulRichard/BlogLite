# 比较并计算字符串的差值

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    写一个函数，实现两个字符串的比较过程。即自己写一个strcmp函数，函数的原型为：int strcmp(char *p1, char *p2)。设p1指向字符串s1，p2指向字符串s2。要求当s1=s2时，返回值为0；若s1≠s2，返回它们二者第一个不同字符的ASCII码差值（例如”BOY”与”BAD”，第二个字母不同，’O’与’A’只差为79-65=14）。如果s1>s2，则输出正值；如果s1<s2，则输出负值。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    有两行，每行有一个不包含空格的字符串，即参与比较的两个字符串。保证每个字符串的长度都不超过200。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    只有一个整数，即strcmp比较两个字符串的返回值。<br /> 请注意行尾输出换行。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int m, n;
int main()
{
    int strcmp(char* p1, char* p2);
    char ch[200], zh[200];
    int t;
    gets(ch);
    gets(zh);
    m = strlen(ch);
    n = strlen(zh);
    t = strcmp(ch, zh);
    printf("%d", t);
    return 0;
}
int strcmp(char* p1, char* p2)
{
    int i, k;
    for (i = 0; i &lt; m; i++)
    {
        if (*(p1 + i) != *(p2 + i))
        {
            k = *(p1 + i) - *(p2 + i);
            return k;
        }
    }
    if (i &gt;= m)
    {
        return 0;
    }
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
