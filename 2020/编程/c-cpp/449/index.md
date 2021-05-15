# 小明A+B(2)

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    小明最近多位数加法运算学的很晕倒：（，幸好是做判断题，它只需要判断A+B最后一位数是否是C就可以了，可是他真的懒的厉害，这不让你写一个程序帮助他
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    两个长度不超过100位整数A B 一个个位数C
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  正确与否,正确是YES 错误则输出NO
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;

int main()
{
    string a, b,a1,b1;
    int c,aa,bb;
    cin &gt;&gt; a &gt;&gt; b &gt;&gt; c;
    a1 = a[0]; b1 = b[0];           //取第一位
    aa = atoi(a1.c_str());          //转换为整形
    bb = atoi(b1.c_str());
    if ((aa + bb)%10 == c)cout &lt;&lt; "YES";
    else cout &lt;&lt; "NO";
    return 0;
}</pre>

&nbsp;
