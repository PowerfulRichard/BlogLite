# 多项式相加

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    一条单链表可以表示一个一元多项式，每个节点包含三个域：指数、系数和后继节点（指针或引用）。
  </p>
  
  <p>
    表示多项式3X<sup>4</sup>-6X<sup>2</sup>+5X-10的单链表如图所示。给定两个多项式，实现两个多项式相加算法。
  </p>
  
  <p>
    <img loading="lazy" src="https://i0.wp.com/acm.webturing.com/JudgeOnline/upload/pimg1170_1.png?resize=600%2C103&#038;ssl=1" alt="" width="600" height="103" data-recalc-dims="1" />
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    第一行输入包含两个整数m,n
  </p>
  
  <p>
    后续为m行和n行数据
  </p>
  
  <p>
    m，n分别代表两个多项式的项数
  </p>
  
  <p>
    后续每一行代表多项式的项，包含a,b两个数据，表示该项的系数和指数。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    从较高指数到较低指数，依次输出求得的和。
  </p>
  
  <p>
    每行一项，格式与输入相同，但无需输出项数，系数为0的项也不输出。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
typedef struct {
    double xs;
    double zs;
} Term;
typedef struct ploy
{
    Term term;
    ploy* next;
} ploy, * LinkList;
void Li(LinkList& L)
{
    L = (ploy*)malloc(sizeof(ploy));
    L-&gt;term.xs = 0.0;
    L-&gt;term.zs = -1;
    L-&gt;next = NULL;
}
int cmp(Term a, Term b)
{
    if (a.zs &lt; b.zs) return 1;
    else if (a.zs == b.zs) return 0;
    else return -1;
}
void in(LinkList& L, Term e)
{
    ploy* q = L;
    while (q-&gt;next != NULL)
    {
        if (cmp(q-&gt;next-&gt;term, e) &lt; 0)
            q = q-&gt;next;
        else break;
    }
    if (q-&gt;next != NULL && cmp(q-&gt;next-&gt;term, e) == 0)
    {
        q-&gt;next-&gt;term.xs += e.xs;
    }
    else
    {
        ploy* node = (ploy*)malloc(sizeof(ploy));
        node-&gt;term.xs = e.xs;
        node-&gt;term.zs = e.zs;
        if (q-&gt;next == NULL)
            node-&gt;next = NULL;
        else
            node-&gt;next = q-&gt;next;
        q-&gt;next = node;
    }
}
void CP(LinkList& L, int m)
{

    Term e;
    Li(L);
    for (int i = 1; i &lt;= m; i++)
    {
        cin &gt;&gt; e.xs &gt;&gt; e.zs;
        in(L, e);
    }
}
void add(LinkList& L1, LinkList& L2)
{
    ploy* q;
    for (q = L2-&gt;next; q != NULL; q = q-&gt;next)
    {
        in(L1, q-&gt;term);
    }
    free(L2);
}
void SubtracatPolyn(LinkList& L1, LinkList& L2)
{
    ploy* q;
    for (q = L2-&gt;next; q != NULL; q = q-&gt;next)
    {
        q-&gt;term.xs = -(q-&gt;term.xs);
        in(L1, q-&gt;term);
    }
    free(L2);
}
void visitList(LinkList L)
{
    ploy* q = L;
    while (q-&gt;next != NULL)
    {
        q = q-&gt;next;
        if (q-&gt;term.xs != 0)
        {
            cout &lt;&lt; q-&gt;term.xs &lt;&lt; " " &lt;&lt; q-&gt;term.zs &lt;&lt; endl;
        }
    }
}
int main()
{
    LinkList L1, L2;
    int n1, n2;
    cin &gt;&gt; n1 &gt;&gt; n2;
    CP(L1, n1);
    CP(L2, n2);
    add(L1, L2);
    visitList(L1);
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
