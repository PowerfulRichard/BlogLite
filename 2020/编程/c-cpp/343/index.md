# 日期计算

## 题目描述 {.page-header.text-muted}

<div class="content">
  写一个函数，给定年、月、日，计算该日期是该年的第几天。在主函数中输入一个日期（含年、月、日），通过函数调用，得到该日期所对应这一年的第几天，并输出该数值。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  三个以空格分隔的整数，分别表示该日期的年、月、日。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输入日期所对应这一年的第几天，一个整数，单独占一行。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int y,m,s,d=0;
    cin&gt;&gt;y&gt;&gt;m&gt;&gt;s;
    switch(m){
        case 12 :
            d=d+30;
            m=m-1;
        case 11:
            d=d+31;
            m=m-1;
        case 10 :
            d=d+30;
            m=m-1;
        case 9 :
            d=d+31;
            m=m-1;
        case 8 :
            d=d+31;
            m=m-1;
        case 7 :
            d=d+30;
            m=m-1;
        case 6 :
            d=d+31;
            m=m-1;
        case 5 :
            d=d+30;
            m=m-1;
        case 4 :
            d=d+31;
            m=m-1;
        case 3 :
            if((y%4!=0)||(y%100==0&&y%400!=0)){
                d=d+28;
                m=m-1;
            }
            else{
                d=d+29;
                m=m-1;
            }
        case 2 :
            d=d+31;
            m=m-1;
        case 1 :
            break;
    }
    d=d+s;
    cout&lt;&lt;d;
    return 0;
}</pre>

&nbsp;
