# 石头剪刀布

## 题目描述 {.page-header.text-muted}

<p class="page-header text-muted">
  编写程序实现“剪刀，石头，布”游戏。在这个游戏中，两个人同时说“剪刀”，“石头”或“布”，压过另一方的为胜者。规则是：“布”胜过“石头”，“石头”胜过“剪刀”，“剪刀”胜过“布”。要求：选择结构中使用枚举类型，结果的输出也使用枚举类型表示。
</p>

## 输入： {.page-header.text-muted}

两个数，范围为{0,1,2}，用空格隔开。0表示石头，1表示布，2表示剪刀。这两个数分别表示两个人所说的物品。

## 输出： {.page-header.text-muted}

如果前者赢，输出1。如果后者赢，输出-1。如果是平局，输出0。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,b;
    while(scanf("%d %d",&a,&b)!=EOF){
        if(a==b){
            cout&lt;&lt;"0"&lt;&lt;endl;
        }
        else if(a==0&&b==2||a==1&&b==0||a==2&&b==1){
            cout&lt;&lt;"1"&lt;&lt;endl;
        }
        else{
            cout&lt;&lt;"-1"&lt;&lt;endl;
        }
    }
    return 0;
}</pre>

&nbsp;
