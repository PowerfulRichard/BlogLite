# Getting Started – Insertion Sort

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Insertion Sort
  </p>
  
  <p>
    Write a program of the Insertion Sort algorithm which sorts a sequence A in ascending order. The algorithm should be based on the following pseudocode:
  </p>
  
  <p>
    for i = 1 to A.length-1
  </p>
  
  <p>
    key = A[i]
  </p>
  
  <p>
    /* insert A[i] into the sorted sequence A[0,&#8230;,j-1] */
  </p>
  
  <p>
    j = i &#8211; 1
  </p>
  
  <p>
    while j >= 0 and A[j] > key
  </p>
  
  <p>
    A[j+1] = A[j]
  </p>
  
  <p>
    j&#8211;
  </p>
  
  <p>
    A[j+1] = key
  </p>
  
  <p>
    Note that, indices for array elements are based on 0-origin.
  </p>
  
  <p>
    To illustrate the algorithms, your program should trace intermediate result for each step.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The first line of the input includes an integer N, the number of elements in the sequence.
  </p>
  
  <p>
    In the second line, N elements of the sequence are given separated by a single space.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  The output consists of N lines. Please output the intermediate sequence in a line for each step. Elements of the sequence should be separated by single space.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp"># include &lt;bits/stdc++.h&gt;
using namespace std;
int a[101];
int n;
void output() {

    for (int i = 0; i &lt; n; i++) {
        if (i + 1 != n)
            cout &lt;&lt; a[i] &lt;&lt; " ";
        else
            cout &lt;&lt; a[i] &lt;&lt; endl;
    }
}
void InsertSort() {
    for (int i = 0; i &lt; n - 1; i++) {
        int temp = a[i + 1];
        for (int j = i; j &gt;= 0; j--) {
            if (temp &lt; a[j]) {
                a[j + 1] = a[j];
                a[j] = temp;
            }
            else {
                break;
            }
        }
        output();
    }

}
int main() {
    cin &gt;&gt; n;
    for (int i = 0; i &lt; n; i++) {
        cin &gt;&gt; a[i];
    }
    output();
    InsertSort();
    return 0;
}</pre>

&nbsp;
