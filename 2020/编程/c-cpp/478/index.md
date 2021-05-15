# 复数加法

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    数集拓展到实数范围内，仍有些运算无法进行。比如判别式小于0的<a href="http://baike.baidu.com/view/397767.htm" target="_blank" rel="noopener">一元二次方程</a>仍<a href="http://baike.baidu.com/view/1203270.htm" target="_blank" rel="noopener">无解</a>，因此将数集再次扩充，达到复数范围。
  </p>
  
  <blockquote>
    <p>
      <b>定义：形如z=a+bi的数称为复数(complex number)</b>
    </p>
  </blockquote>
  
  <p>
    其中规定<b>i</b>为<b>虚数单位</b>，且i^2=i*i=-1（a，b是任意<a href="http://baike.baidu.com/view/14749.htm" target="_blank" rel="noopener">实数</a>）
  </p>
  
  <p>
    我们将复数z=a+bi中的实数a称为复数z的实部（real part)记作Rez=a
  </p>
  
  <p>
    实数b称为复数z的<a href="http://baike.baidu.com/view/2441262.htm" target="_blank" rel="noopener">虚部</a>（imaginary part)记作 Imz=b.
  </p>
  
  <p>
    已知：当b=0时，z=a，这时复数成为实数；
  </p>
  
  <p>
    当a=0且b≠0时 ，z=bi，我们就将其称为<a href="http://baike.baidu.com/view/899964.htm" target="_blank" rel="noopener"><b>纯虚数</b></a>。
  </p>
  
  <blockquote>
    <p>
      <b>定义： 对于复数z=a+bi，称复数z&#8217;=a-bi为z的</b><a href="http://baike.baidu.com/view/137793.htm" target="_blank" rel="noopener"><b>共轭复数</b></a><b>。</b>
    </p>
    
    <p>
      <b>定义：将复数的实部与虚部的平方和的正的平方根的值称为该复数的模，记作∣z∣</b>
    </p>
  </blockquote>
  
  <p>
    即对于复数z=a+bi，它的模
  </p>
  
  <p>
    ∣z∣=√(a^2+b^2)
  </p>
  
  <p>
    复数的集合用C表示，显然，R是C的真子集
  </p>
  
  <p>
    复数集是无序集，不能建立大小顺序。
  </p>
  
  <p>
    共轭复数有些有趣的性质: ︱x+yi︱=︱x-yi︱ (x+yi)*(x-yi)=x^2+y^2=︱x+yi︱^2=︱x-yi︱^2
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    两个复数分两行，每行两个整数r,i，代表复数的实部和虚部。|r,i|<=10^9
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    两个复数的和。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct Complex {
    int real;
    int image;
};
void input(Complex&c) {
    cin&gt;&gt;c.real&gt;&gt;c.image;
}
void disp(Complex c) {
    cout&lt;&lt;c.real&lt;&lt;" "&lt;&lt;c.image;
}
Complex add(Complex a,Complex b) {
    Complex c;
    c.real=a.real+b.real;
    c.image=a.image+b.image;
    return c;
}
int main() {
    Complex a,b;
    input(a);
    input(b);
    disp(add(a,b));
    return 0;
}</pre>

&nbsp;
