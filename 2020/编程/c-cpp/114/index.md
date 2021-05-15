# 成绩转换

解法一：只使用if语句

<pre class="EnlighterJSRAW" data-enlighter-language="cpp" data-enlighter-theme="godzilla">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(void)
{
    int a;
    while (scanf("%d", &a) != EOF) {
        if (a &gt;= 90 && a &lt;= 100) {
            cout &lt;&lt; "A" &lt;&lt; endl;
        }
        else if (a &gt;= 80 && a &lt;= 89) {
            cout &lt;&lt; "B" &lt;&lt; endl;
        }
        else if (a &gt;= 70 && a &lt;= 79) {
            cout &lt;&lt; "C" &lt;&lt; endl;
        }
        else if (a &gt;= 60 && a &lt;= 69) {
            cout &lt;&lt; "D" &lt;&lt; endl;
        }
        else if (a &gt;= 0 && a &lt;= 59) {
            cout &lt;&lt; "E" &lt;&lt; endl;
        }
        else {
            cout &lt;&lt; "Score is error!" &lt;&lt; endl;
        }
    }
    return 0;
}</pre>

解法二：使用switch语句

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n;
    char s;
    while(scanf("%d",&n)!=EOF){
        if(n&gt;=80){s='a';}
        if(n&gt;=70&&n&lt;=79){s='b';}
        if(n&gt;=60&&n&lt;=69){s='c';}
        if(n&lt;60&&n&gt;=0){s='d';}
        if(n&lt;0||n&gt;100){s='e';}
        switch(s){
            case 'a' :
                printf("A\n");break;
            case 'b' :
                printf("B\n");break;
            case 'c' :
                printf("C\n");break;
            case 'd' :
                printf("D\n");break;
            case 'e' :
                printf("E\n");break;
            default :
                printf("Score is error\n");break;
        }
    }
    
    return 0;
}</pre>

&nbsp;
