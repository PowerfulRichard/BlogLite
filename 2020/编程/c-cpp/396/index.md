# Array – Matrix Vector Multiplication

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Matrix Vector Multiplication
  </p>
  
  <p>
    Write a program which reads a n×m matrix A and a m×1 vector b, and prints their product Ab.
  </p>
  
  <p>
    A column vector with m elements is represented by the following equation.
  </p>
  
  <p>
    A n×m matrix with mm column vectors, each of which consists of n elements, is represented by the following equation.
  </p>
  
  <p>
    i-th element of a m×1 column vector b is represented by bi (i=1,2,&#8230;,m), and the element in i-th row and j-th column of a matrix A is represented by aij (i=1,2,&#8230;,n,j=1,2,&#8230;,m).
  </p>
  
  <p>
    The product of a n×m matrix A and a m×1 column vector b is a n×1 column vector c, and ci is obtained by the following formula:
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  In the first line, two integers n and m are given. In the following n lines, aij are given separated by a single space character. In the next mm lines, bi is given in a line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  The output consists of n lines. Print ci in a line.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include &lt;stdio.h&gt;

int main() {
    int m, n, t;
    scanf("%d%d", &m, &n);
    int a1[m][n], a2[n];
    for (int a = 0; a &lt; m; ++a) {
        for (int b = 0; b &lt; n; ++b) {
            scanf("%d", &t);
            a1[a][b] = t;
        }
    }
    for (int a = 0; a &lt; n; ++a) {
        scanf("%d", &t);
        a2[a] = t;
    }
    for (int i = 0; i &lt; m; ++i) {
        int sum=0;
        for (int k = 0; k &lt; n; ++k) {
            sum += a1[i][k]*a2[k];
        }
        printf("%d\n", sum);
    }
}</pre>

&nbsp;
