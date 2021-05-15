# Sort I – Bubble Sort

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Bubble Sort
  </p>
  
  <p>
    Write a program of the Bubble Sort algorithm which sorts a sequence A in ascending order. The algorithm should be based on the following pseudocode:
  </p>
  
  <p>
    BubbleSort(A)
  </p>
  
  <p>
    1 for i = 0 to A.length-1
  </p>
  
  <p>
    2   for j = A.length-1 downto i+1
  </p>
  
  <p>
    3      if A[j] < A[j-1]
  </p>
  
  <p>
    4          swap A[j] and A[j-1]
  </p>
  
  <p>
    Note that, indices for array elements are based on 0-origin.
  </p>
  
  <p>
    Your program should also print the number of swap operations defined in line 4 of the pseudocode.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The first line of the input includes an integer N, the number of elements in the sequence.
  </p>
  
  <p>
    In the second line, N elements of the sequence are given separated by spaces characters.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    The output consists of 2 lines.
  </p>
  
  <p>
    In the first line, please print the sorted sequence. Two contiguous elements of the sequence should be separated by a space character.
  </p>
  
  <p>
    In the second line, please print the number of swap operations.
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int bubble_sort(int a[], int n)
{
    int cnt = 0;

    for (int i = 0; i &lt; n - 1; i++)
        for (int j = n - 1; j &gt;= i + 1; j--)
            if (a[j] &lt; a[j - 1])
                cnt++, swap(a[j], a[j - 1]);

    return cnt;
}
void output_result(int a[], int n)
{
    for (int i = 0; i &lt; n; i++) {
        if (i &gt; 0)
            cout &lt;&lt; " ";
        cout &lt;&lt; a[i];
    }
    cout &lt;&lt; endl;
}
const int N = 100;
int a[N];
int main()
{
    int n;
    cin &gt;&gt; n;
    for (int i = 0; i &lt; n; i++)
        cin &gt;&gt; a[i];
    int cnt = bubble_sort(a, n);
    output_result(a, n);
    cout &lt;&lt; cnt &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
