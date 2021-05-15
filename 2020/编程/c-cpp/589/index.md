# 删数问题

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    给定 n 位正整数 a，去掉其中任意 k≤n 个数字后，剩下的数字按原次序排列组成一个新的正整数。对于给定的 n 位正整数 a 和正整数 k，设计一个算法找出剩下数字组成的新数最小的删数方案。
  </p>
  
  <blockquote>
    <p>
      <strong>算法设计：</strong><br /> 对于给定的正整数 a，计算删去 k 个数字后得到的最小数。
    </p>
  </blockquote>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入第 1 行是 1 个正整数 a。第 2 行是正整数 k。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出最小数</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
#define L 101
int main() {
    int i, j, k, m, n, t, c;
    char ch[L], s;
    while (~scanf("%s %d", ch, &n)) {
        while (n--)
        {
            m = strlen(ch);
            for (i = 0; i &lt; m; i++)
            {
                if (ch[i] &gt; ch[i + 1])
                {
                    for (j = i; ch[j] != 0; j++)
                    {
                        ch[j] = ch[j + 1];
                    }
                    break;
                }
            }
        }
        c = 0;
        for (i = 0; ch[i] != 0; i++) {
            if (ch[i] != '0' || (ch[i] == '0' && c)) {
                printf("%c", ch[i]);
                c++;
            }
        }
        if (c)printf("\n");
        else printf("0\n");
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
