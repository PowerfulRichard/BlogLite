# 八皇后问题

## 题目描述 {.page-header.text-muted}

<div class="content">
  经典的八皇后问题，在一个8*8的棋盘上放置8个皇后，使得不能互相攻击到，皇后的攻击范围的同一行，同一列以及同一个斜线。要求输出所有不会互相攻击到的摆放方式，所有通过旋转，对称都方式得到的摆放方式均认为是不同的摆放方式。棋盘被编号为0-7行，0-7列。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  无输入。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  每行一个数字代表摆放方式，如01234567代表从第0行放在0列，第1行放在1列，<br /> 第2行放在2列，按照升序输出。</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
#define max 8
int queen[max], sum=0; 
 
void show() 
{
    int i;
    for(i = 0; i &lt; max; i++)
    {
         printf("%d", queen[i]);
    }
    printf("\n");
    sum++;
}
 
int PLACE(int n) 
{
    int i;
    for(i = 0; i &lt; n; i++) 
    {
        if(queen[i] == queen[n] || abs(queen[i] - queen[n]) == (n - i))
        {
            return 1;
        }
    }
    return 0;
}
 
void NQUEENS(int n)
{
    int i;
    for(i = 0; i &lt; max; i++)
    {
        queen[n] = i;
        if(!PLACE(n))
        {
            if(n == max - 1)
            {
                show(); 
            }
            else
            {
                NQUEENS(n + 1); 
            }
        }
    }
}
 
int main()
{
    NQUEENS(0); 
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
