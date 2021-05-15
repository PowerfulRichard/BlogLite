# 一种排序

### **题目描述** {.page-header.text-muted}

<div class="content">
  <p>
    现在有很多长方形，每一个长方形都有一个编号，这个编号可以重复；还知道这个长方形的宽和长，编号、长、宽都是整数；现在要求按照一下方式排序（默认排序规则都是从小到大）；
  </p>
  
  <p>
    1.按照编号从小到大排序
  </p>
  
  <p>
    2.对于编号相等的长方形，按照长方形的长排序；
  </p>
  
  <p>
    3.如果编号和长都相同，按照长方形的宽排序；
  </p>
  
  <p>
    4.如果编号、长、宽都相同，就只保留一个长方形用于排序,删除多余的长方形；最后排好序按照指定格式显示所有的长方形；
  </p>
</div>

### **输入** {.page-header.text-muted}

<div class="content">
  <p>
    第一行有一个整数 0<n<10000,表示接下来有n组测试数据； <br=&#8221;&#8221;>每一组第一行有一个整数 0<m<1000，表示有m个长方形； <br=&#8221;&#8221;>接下来的m行，每一行有三个数 ，第一个数表示长方形的编号，第二个和第三个数值大的表示长，数值小的表示宽相等，说明这是一个正方形（数据约定长宽与编号都小于10000）；</m<1000，表示有m个长方形；></n<10000,表示接下来有n组测试数据
  </p>
</div>

### **输出** {.page-header.text-muted}

<div class="content">
  顺序输出每组数据的所有符合条件的长方形的 编号 长 宽
</div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;iostream&gt;
#include &lt;algorithm&gt;

using namespace std;

struct node {
    int number, len, width;
}P[1005];

bool cmp (node a, node b) {
    if (a.number != b.number) return a.number&lt;b.number;
    if (a.len != b.len) return a.len&lt;b.len;
    return a.width&lt;b.width;
}

int main() {
    int N;
    cin &gt;&gt;N;
    while (N --) {
        int m;
        cin &gt;&gt;m;
        for (int i=0; i&lt;m; ++i) {
            int a, b, c;
            cin &gt;&gt;a &gt;&gt;b &gt;&gt;c;
            P[i].number = a;
            P[i].len = max(b, c); 
            P[i].width = min(b, c);
        }

        sort (P, P+m, cmp);
        cout &lt;&lt;P[0].number &lt;&lt;" " &lt;&lt;P[0].len &lt;&lt;" " &lt;&lt;P[0].width &lt;&lt;endl;
        for (int i=1; i&lt;m; ++i) {
            if (P[i].number == P[i-1].number && P[i].len == P[i-1].len && P[i].width == P[i-1].width) continue;
            cout &lt;&lt;P[i].number &lt;&lt;" " &lt;&lt;P[i].len &lt;&lt;" " &lt;&lt;P[i].width &lt;&lt;endl;
        }
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
