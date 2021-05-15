# Lucky Words

## 题目描述 {.page-header.text-muted}

<div class="content">
  如果-个数 n 能被各位数字之和整除，那么这个数就是 Lucky Word。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    多组输入
  </p>
  
  <p>
    每行一个数n
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  如果这个数是Lucky Word 那么输出 &#8220;Lucky Word&#8221;,否则输出 &#8220;No Answer&#8221;。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;stdio.h&gt;
int main()
{
    int n, a, b, i = 1;
    int c[100];
    while (1 == scanf("%d", &n))
    {
        int s = 0;
        a = n % 10;
        b = n / 10;
        while (b != 0)
        {
            c[i] = b % 10;
            b = b / 10;
            s = s + c[i];
            i++;
        }
        s = s + a;
        if (n % s == 0)
        {
            printf("Lucky Word\n");
        }
        else
        {
            printf("No Answer\n");
        }
    }
    return 0;
}</pre>

&nbsp;
