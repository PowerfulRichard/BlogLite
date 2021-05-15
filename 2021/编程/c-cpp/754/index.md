# C++面向对象：入门

# 题目

设计一个类complex，对复数进行输出。其中有两个数据成员realPart和imagePart分别表示复数的实部和虚部；提供一个成员函数set，为类数据成员赋值；提供一个成员函数print，将该类对象以realPart+imagePart*i的方式输出。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;iostream&gt;
using namespace std;
class Complex {
private:
    int realPart; int imagePart;
public:
    void Set(int realPart, int imagePart);
    void Print();
};
void Complex::Set(int a, int b){
    realPart = a;
    imagePart = b;
}
void Complex::Print() {
    cout &lt;&lt; realPart &lt;&lt; "+" &lt;&lt; imagePart &lt;&lt; "*i" &lt;&lt; endl;
}
int main() {
    Complex Number;
    int x, y;
    cin &gt;&gt; x &gt;&gt; y;
    Number.Set(x, y);
    Number.Print();
    return 0;
}</pre>

&nbsp;

&nbsp;

&nbsp;
