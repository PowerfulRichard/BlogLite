# 数组计算缺失的扑克牌Array – Finding Missing Cards

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Finding Missing Cards
  </p>
  
  <p>
    Taro is going to play a card game. However, now he has only n cards, even though there should be 52 cards (he has no Jokers).
  </p>
  
  <p>
    The 52 cards include 13 ranks of each of the four suits: spade, heart, club and diamond.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    In the first line, the number of cards n (n ≤ 52) is given.
  </p>
  
  <p>
    In the following n lines, data of the n cards are given. Each card is given by a pair of a character and an integer which represent its suit and rank respectively. A suit is represented by &#8216;S&#8217;, &#8216;H&#8217;, &#8216;C&#8217; and &#8216;D&#8217; for spades, hearts, clubs and diamonds respectively. A rank is represented by an integer from 1 to 13.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    Print the missing cards. The same as the input format, each card should be printed with a character and an integer separated by a space character in a line. Arrange the missing cards in the following priorities:
  </p>
  
  <p>
    Print cards of spades, hearts, clubs and diamonds in this order.
  </p>
  
  <p>
    If the ranks are equal, print cards with lower ranks first.
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n;
    int s[13],h[13],c[13],d[13];
    int ss=0,hh=0,cc=0,dd=0;
    char t;
    cin&gt;&gt;n;
    while(n--){
        cin&gt;&gt;t;
        switch(t){
            case 'S' :
            cin&gt;&gt;s[ss];
            ss++;
            break;
            case 'H' :
            cin&gt;&gt;h[hh];
            hh++;
            break;
            case 'C' :
            cin&gt;&gt;c[cc];
            cc++;
            break;
            case 'D' :
            cin&gt;&gt;d[dd];
            dd++;
            break;
        }
    }
    sort(s,s+ss);
    sort(h,h+hh);
    sort(c,c+cc);
    sort(d,d+dd);
    for (int i = 1, j = 0; i &lt;= 13; i++)
    {
        if (s[j] != i)
            cout &lt;&lt; "S " &lt;&lt; i &lt;&lt; endl;
        else
            ++j;
    }
    for (int i = 1, j = 0; i &lt;= 13; i++)
    {
        if (h[j] != i)
            cout &lt;&lt; "H " &lt;&lt; i &lt;&lt; endl;
        else
            ++j;
    }
    for (int i = 1, j = 0; i &lt;= 13; i++)
    {
        if (c[j] != i)
            cout &lt;&lt; "C " &lt;&lt; i &lt;&lt; endl;
        else
            ++j;
    }
    for (int i = 1, j = 0; i &lt;= 13; i++)
    {
        if (d[j] != i)
            cout &lt;&lt; "D " &lt;&lt; i &lt;&lt; endl;
        else
            ++j;
    }
    return 0;
}</pre>

&nbsp;
