# 输出倒序数组（数组元素逆置）

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    将一个长度为10的整型数组中的值按逆序重新存放。
  </p>
  
  <p>
    如：原来的顺序为1,2,3,4,5,6,7,8,9,0，要求改为0,9,8,7,6,5,4,3,2,1
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    从键盘上输入以空格分隔的10个整数。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  按相反的顺序输出这10个数，每个数占一行。
</div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a[10];
    int i;
    for(i=0;i&lt;10;i++){
        scanf("%d",&a[i]);
    }
    for(i=9;i&gt;=0;i--){
        printf("%d ",a[i]);
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
