# 多项式相加

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;iostream&gt;
#include &lt;map&gt;
using namespace std;
struct ploy {
    int m;
    map&lt;int, int&gt; mp;
    void input() {
        for (int i = 0; i &lt; m; i++) {
            int coef, index;
            cin &gt;&gt; coef &gt;&gt; index;
            mp[index] = coef;
        }
    }
    void add(ploy &that) {
        this-&gt;m = this-&gt;m &gt; that.m ? this-&gt;m : that.m;
        for (int i = 0; i &lt;= m; i++) mp[i] += that.mp[i];
    }
    void disp() {
        for (int i = m; i &gt;= 0; i--)
            if (mp[i]) cout &lt;&lt; mp[i] &lt;&lt; " " &lt;&lt; i &lt;&lt; endl;
    }
};
int main(int argc, char const *argv[]) {

    for (ploy a, b; cin &gt;&gt; a.m &gt;&gt; b.m;) {
        a.input();
        b.input();
        a.add(b);
        a.disp();
    }
    return 0;
}
</pre>

&nbsp;
