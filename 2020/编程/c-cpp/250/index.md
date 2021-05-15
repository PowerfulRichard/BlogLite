# 角谷猜想

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    角谷猜想:<br /> 日本一位中学生发现一个奇妙的“定理”，请角谷教授证明，而教授无能为力，于是产生角谷猜想。猜想的内容是：任给一个自然数，若为偶数除以2，若为奇数则乘3加1，得到一个新的自然数后按照上面的法则继续演算，若干次后得到的结果必然为1。请编程验证。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    任一正整数 n  范围[2,1000000]
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    演算的过程
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="c">#include &lt;stdio.h&gt;
main()
{
    long long n;
    scanf("%lld",&n);
    while(n!=1)
    {
        if(n%2==0)
        {
            printf("%lld/2=%lld\n",n,n/2);
            n/=2;
        }
        else
        {
            printf("%lld*3+1=%lld\n",n,n*3+1);
            n=n*3+1;
        }
    }
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
