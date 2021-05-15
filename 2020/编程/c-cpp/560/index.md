# Sort I-Selection Sort

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Selection Sort
  </p>
  
  <p>
    Write a program of the Selection Sort algorithm which sorts a sequence A in ascending order. The algorithm should be based on the following pseudocode:
  </p>
  
  <p>
    SelectionSort(A)
  </p>
  
  <p>
    1 for i = 0 to A.length-1
  </p>
  
  <p>
    2     mini = i
  </p>
  
  <p>
    3    for j = i to A.length-1
  </p>
  
  <p>
    4           if A[j] < A[mini]
  </p>
  
  <p>
    5               mini = j
  </p>
  
  <p>
    6     swap A[i] and A[mini]
  </p>
  
  <p>
    Note that, indices for array elements are based on 0-origin.
  </p>
  
  <p>
    Your program should also print the number of swap operations defined in line 6 of the pseudocode in the case where i ≠ mini.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    The first line of the input includes an integer N, the number of elements in the sequence.
  </p>
  
  <p>
    In the second line, N elements of the sequence are given separated by space characters.
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
typedef long long ll;
using namespace std;
int a[110];
int main(){
    ios::sync_with_stdio(false);
    int n;
    cin&gt;&gt;n;
    for(int i = 1 ; i&lt;=n ; i++){
        cin&gt;&gt;a[i];
    }
    
    int ans = 0;
    for(int i = 1 ; i&lt;=n-1 ; i++){
        int min = a[i];
        int flag = i;
        for(int j = i+1 ; j&lt;=n ; j++){
            if(min &gt; a[j]){
                flag = j;
                min = a[j];
            }
        } 
        if(flag != i){
            swap(a[flag] , a[i] );
            ans++;
        }
    }
    for(int i = 1 ; i&lt;=n ; i++){
        if(i == 1)
            cout&lt;&lt;a[i];
        else{
            cout&lt;&lt;" "&lt;&lt;a[i];
        }
    }
    cout&lt;&lt;endl;
    cout&lt;&lt;ans&lt;&lt;endl;
    return 0;
}</pre>

&nbsp;
