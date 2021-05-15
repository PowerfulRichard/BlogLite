# 候选人得票

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    完成一个对候选人得票的统计程序。假设有3个候选人，名字分别为Li，Zhang和Fun。使用结构体存储每一个候选人的名字和得票数。记录每一张选票的得票人名，输出每个候选人最终的得票数。结构体可以定义成如下的格式：<br /> struct person {<br /> char name[20];<br /> int count;<br /> }leader[3] = {&#8220;Li&#8221;, 0, &#8220;Zhang&#8221;, 0, &#8220;Fun&#8221;, 0};
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    第一行有一个整数n，表示以下有n张选票信息将会输入。保证n不大于100。<br /> 以后的n行中，每一行包含一个人名，为选票的得票人。保证每一个人名都是Li，Zhang和Fun中的某一个。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    有三行，分别为Li，Zhang和Fun每人的得票数。格式为首先输出人名，其后输出一个冒号，最后输出候选人的得票数。<br /> 请注意行尾输出换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct person{
    char name[20];
    int count;
}leader[3]={"Li",0,"Zhang",0,"Fun",0};
int main(){
    int n;
    char name1[20];
    scanf("%d",&n);
    for(int i=0;i&lt;n;i++){
    scanf("%s",name1);
    for(int j=0;j&lt;3;j++){
        if(strcmp(leader[j].name,name1)==0)
        leader[j].count++;
    }
    }
    
    printf("Li:%d\n",leader[0].count);
    printf("Zhang:%d\n",leader[1].count);
    printf("Fun:%d",leader[2].count);
    return 0;
}</pre>

&nbsp;
