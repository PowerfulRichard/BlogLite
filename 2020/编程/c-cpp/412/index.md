# Array – Official House

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    You manage 4 buildings, each of which has 3 floors, each of which consists of 10 rooms. Write a program which reads a sequence of tenant/leaver notices, and reports the number of tenants for each room.
  </p>
  
  <p>
    For each notice, you are given four integers b, f, r and v which represent that v persons entered to room r of fth floor at building b. If v is negative, it means that v persons left.
  </p>
  
  <p>
    Assume that initially no person lives in the building.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  In the first line, the number of notices n is given. In the following n lines, a set of four integers b, f, r and v which represents ith notice is given in a line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  For each building, print the information of 1st, 2nd and 3rd floor in this order. For each floor information, print the number of tenants of 1st, 2nd, .. and 10th room in this order. Print a single space character before the number of tenants. Print &#8220;####################&#8221; (20 &#8216;#&#8217;) between buildings.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;bits/stdc++.h&gt;
using namespace std;
int B[4][3][10];
int main() {
    int n,b, f, r, v;   
    cin &gt;&gt; n;
    while (n--) {
        cin &gt;&gt; b &gt;&gt; f &gt;&gt; r &gt;&gt; v;
        B[b - 1][f - 1][r - 1] += v;
    }
    for (int i = 0; i &lt; 4; i++) {
        for (int j = 0; j &lt; 3; j++) {
            for (int k = 0; k &lt; 10; k++) {
                cout &lt;&lt;" ";
                cout &lt;&lt; B[i][j][k];
            }
            cout &lt;&lt; endl;
        }
        if (i &lt; 3) {
            cout &lt;&lt; "####################" &lt;&lt; endl;
        }
    }
    return 0;
}</pre>

&nbsp;
