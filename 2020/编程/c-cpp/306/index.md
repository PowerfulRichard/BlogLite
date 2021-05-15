# The 3n+1 Problem

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Problems in Computer Science are often classified as belonging to a certain class of problems (e.g., NP, Unsolvable, Recursive). In this problem you will be analyzing a property of an algorithm whose classification is not known for all possible inputs.<br /> Consider the following algorithm:<br /> 1. input n<br /> 2. print n<br /> 3. if n = 1 then STOP<br /> 4. if n is odd then n <- 3n + 1<br /> 5. else n <- n / 2<br /> 6. GOTO 2<br /> Given the input 22, the following sequence of numbers will be printed 22 11 34 17 52 26 13 40 20 10 5 16 8 4 2 1<br /> It is conjectured that the algorithm above will terminate (when a 1 is printed) for any integral input value. Despite the simplicity of the algorithm, it is unknown whether this conjecture is true. It has been verified, however, for all integers n such that 0 < n < 1,000,000 (and, in fact, for many more numbers than this.)<br /> Given an input n, it is possible to determine the number of numbers printed (including the 1). For a given n this is called the cycle-length of n. In the example above, the cycle length of 22 is 16.<br /> For any two numbers i and j you are to determine the maximum cycle length over all numbers between i and j.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The input will consist of a series of pairs of integers i and j, one pair of integers per line. All integers will be less than 1,000,000 and greater than 0.<br /> You should process all pairs of integers and for each pair determine the maximum cycle length over all integers between and including i and j.<br /> You can assume that no opperation overflows a 32-bit integer.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    For each pair of input integers i and j you should output i, j, and the maximum cycle length for integers between and including i and j. These three numbers should be separated by at least one space with all three numbers on one line and with one line of output for each line of input. The integers i and j must appear in the output in the same order in which they appeared in the input and should be followed by the maximum cycle length (on the same line).
  </p>
  
  <blockquote>
    <p>
      中文大意：输入多组i,j，分别计算i~j之间的所有数字运算3n+1所需要的步骤次数，输出最大的次数
    </p>
  </blockquote>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int i,j,n=1,z=0,x,ii;       //n存储每轮次数，z比较最大次数，x用于计算单次3n+1循环 
    while(scanf("%d %d",&i,&j)!=EOF) {
        ii=i;       //ii存储i的初始值 
        while(i&lt;=j) {
            x=i;
            while(x!=1) {
                if(x%2==0) {
                    x=x/2;
                    n++;
                } else {
                    x=x*3+1;
                    n++;
                }
            }
            if(n&gt;z){
                z=n;
            }
            n=1;
            i=i+1;
        }
        cout&lt;&lt;ii&lt;&lt;" "&lt;&lt;j&lt;&lt;" "&lt;&lt;z&lt;&lt;endl;
        z=0; 
    }
    return 0;
}</pre>

&nbsp;
