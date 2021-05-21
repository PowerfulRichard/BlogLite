# SSR


## 题目描述
{{< admonition type=quote title="" open=true >}}
事情，是这样的。
有这么一天双休日的中午。
我刚把我衣服扔进了洗衣机，然后拿了个小板凳坐在旁边发呆。
然后突然想到这么无聊干脆玩会阴阳师好了，于是从斗篷帽子里掏出我的手机登录了阴阳师。
看着更新公告里写着的新SSR式神一目连感叹了一下：我要是能有个一目连该多好啊
看了一眼我家帅气的扛把子咕咕，正准备肝困难的时候发现庭院里那一串灯笼里的调查问卷有蝴蝶在绕，于是点进去填了一波在最结尾写上了我当时的愿望：我想要一目连。
然后奖励了一个符，顺手就抽了。本来以为又是R卡，没想到手机震动了一下。
握草！！！一目连！！！！
当时我就激动的站了起来使劲看了一眼然后仰天大笑以及截图装逼。
{{< /admonition >}}

{{< admonition type=question title="问题" open=true >}}
SSR全称为superior super rare，特级超稀有。一般为卡牌类游戏最高稀有等级。
题目是给出三个字符，求其升级到SSR所需要的次数。
最小为AAA，最大为SSR；
SSQ升级到SSR需要升级1次，
SRR升级到SSR需要升级19次。
{{< /admonition >}}

## 输入

第一行输入一个整数T（代表T组数据）

接下来T行，包含3个连续的大写字母（A~S）

## 输出

每个样例输出一行
升级到SSR所需的次数

## 样例输入
```
3
SSR
SRR
AAA
```
## 样例输出
```
0
19
6857
```

---
{{< admonition type=info title="提示" open=true >}}
SRR升级到SSR的过程：  
SRR -> SRS -> SSA ->SSB -> SSC -> ……->SSR 共19次
{{< /admonition >}}

{{< admonition type=tip title="解法" open=true >}}
本质上可看做19进制换算
{{< /admonition >}}


## 题解
```cpp
#include <iostream>
#include <algorithm>
#include <cstring>
using namespace std;
int change(char n){
    switch(n){
        case 'A':return 0;
        case 'B':return 1;
        case 'C':return 2;
        case 'D':return 3;
        case 'E':return 4;
        case 'F':return 5;
        case 'G':return 6;
        case 'H':return 7;
        case 'I':return 8;
        case 'J':return 9;
        case 'K':return 10;
        case 'L':return 11;
        case 'M':return 12;
        case 'N':return 13;
        case 'O':return 14;
        case 'P':return 15;
        case 'Q':return 16;
        case 'R':return 17;
        case 'S':return 18;
        default :return -1;
    }
}
double power(double x, int n)
{
    double val = 1.0;
    while (n--)
        val *= x;
    return val;
}
int main() {
    int num;
    cin>>num;
    while(num--){
    char a,b,c;
    cin>>a>>b>>c;
    int t;
    t=change(a)*power(19,2)+change(b)*power(19,1)+change(c)*power(19,0);
    cout<<6857-t<<endl;
    }
    return 0;
}
```
