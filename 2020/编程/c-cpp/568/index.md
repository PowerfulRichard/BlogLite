# 字符串的字典序排序

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    在main函数中输入10个不等长的字符串，另外写一个函数对它们按字典序从小到大排序。并在main函数中输出这10个已经排好序的字符串。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    共有10行，每行一个字符串。输入保证每行的字符串长度不超过100个字符。请注意字符串中有可能包含空格。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    与输入格式相同，每行输出一个排好序之后的字符串。<br /> 请注意行尾输出换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
static void ranks(char* p)
{
    int i, j, k = 0;
    char temp[50];
    for (i = 0; i &lt; 9; i++)
    {
        k = i;
        for (j = i + 1; j &lt; 10; j++)
            if (strcmp(p + k * 50, p + j * 50) &gt; 0)
                k = j;
        if (k != i)
        {
            strcpy(temp, p + i * 50);
            strcpy(p + i * 50, p + k * 50);
            strcpy(p + k * 50, temp);
        }
    }
}
int main()
{
    char str[10][50];
    int i;
    char* p = str[0];
    for (i = 0; i &lt; 10; i++)
    {

        gets(str[i]);
    }
    ranks(p);
    for (i = 0; i &lt; 10; i++)
        printf("%s\n", str[i]);

    return 0;
}</pre>

&nbsp;
