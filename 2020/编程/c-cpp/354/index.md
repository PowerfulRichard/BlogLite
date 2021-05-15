# 输出回文素数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">小王对既是素数又是回文的数特别感兴趣。比如说151既是素数又是个回文。现在小王想要你帮助他找出某个范围内的素数回文数，请你写个程序找出 a 跟b 之间满足条件的数。(5 <= a < b <= 100,000,000);</span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">输入a和b</span><span style="font-family: Times New Roman; font-size: medium;">(5 <= a < b <= 100,000,000)</span>
  </p>
  
  <h4>
    <a href="http://pan.zekun.fun/file/13327980-471016004">模块法</a>
  </h4>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
bool primer(int n){             //定义布尔函数：判断素数（primer） 
    if(n==2)return true;        //n为2时返回 真 
    if(n&lt;2||n%2==0)return false;//n小于2或n为偶数返回 假 
    
    for(int c=3;c*c&lt;=n;c+=2){    //n有因数返回 假 
        if(n%c==0)return false;
    }
    return true;                //不是上面的情况返回 真 
}
int reverse(int n){             //将数字反转 
    int m=0;
    while(n&gt;0){
        m=m*10+n%10;
        n/=10;
    }
    return m;
}
bool sysmetric(int n){          //判断回文数（引用上面“数字反转”函数，当反转数字与原数字相同时为回文数） 
    return n==reverse(n);
}
int main(){
    int a,b;
    cin&gt;&gt;a&gt;&gt;b;
    for(int x=a;x&lt;=b;x++){
        if(primer(x)&&sysmetric(x)){    //引用函数，当输入的数字都符合条件时会返回真 
            cout&lt;&lt;x&lt;&lt;endl;      //当两个函数都返回真时，if语句才会被执行
        }
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
  
  <p>
    <span style="color: #353535; font-size: 1.25em; font-weight: bold;">暴力法</span>
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
using namespace std;
int huiwen(int z) 
{ 
    int j,i,n; 
    char a[9],b[9]; 
    sprintf(a,"%d",z);
    n=strlen(a);
    for(i=0,j=n-1;i&lt;n;i++,j--)
        b[j]=a[i];
    for(i=0;i&lt;n;i++) 
    { 
        if(b[i]!=a[i]) 
         break;
    } 
    if(i==n)return z;
    else return 0;
    return 0; 
}

int main(){
    int x,y;
    int n,a=0;
    int i=1;
    int h;
    while(scanf("%d %d",&x,&y)!=EOF){
        n=x;
        while(n&lt;=y){
            for(;n&gt;i;i++){
                if(n%i==0){
                    a++;
                }
            }
            if(a==1){
                h=huiwen(n);
                if(h!=0){
                    cout&lt;&lt;n&lt;&lt;endl;
                }
            }
            n++;i=1;a=0;
        }
    }
    return 0;
}</pre>

&nbsp;
