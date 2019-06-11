---


---

<h1 id="histogram-analysis">Histogram Analysis</h1>
<h2 id="step-0--list-contains-some-numbers">Step 0 : <em>List contains some numbers</em></h2>
<ul>
<li>Create a numbers list that contains some unique numbers</li>
<li>Display the list</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python">numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">8</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span>
<span class="token keyword">print</span><span class="token punctuation">(</span>numbers<span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">[2, 4, 5, 1, 6, 7, 8, 3]
</code></pre>
<h2 id="step-1--list-contains-some-duplicate-numbers">Step 1 : <em>List contains some duplicate numbers</em></h2>
<ul>
<li>Create a numbers list that contains some numbers and that constains duplicates</li>
<li>Display the list</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python">numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">8</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span>
<span class="token keyword">print</span><span class="token punctuation">(</span>numbers<span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">[2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
</code></pre>
<h2 id="step-2--finding-the-each-numbers-count-and-display">Step 2 : <em>Finding the each numbers count and display</em></h2>
<ul>
<li>Create a numbers list that contains some numbers and that constains duplicates</li>
<li>Display the list</li>
<li>Display the counts of each number</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">8</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"List contain :"</span><span class="token punctuation">,</span> numbers<span class="token punctuation">)</span>
histo <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> numbers<span class="token punctuation">:</span>
   histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Count of each number in the list"</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"--------------------------------"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> histo<span class="token punctuation">:</span>
   <span class="token keyword">print</span><span class="token punctuation">(</span>key<span class="token punctuation">,</span> <span class="token string">"--"</span><span class="token punctuation">,</span>histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">List contain : [2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
Count of each number in the list
--------------------------------
2 -- 1
4 -- 2
5 -- 1
1 -- 2
6 -- 1
7 -- 2
8 -- 1
3 -- 2
</code></pre>
<h2 id="step-3--finding-the-each-numbers-count-and-display-like-a-graph-histogram">Step 3 : <em>Finding the each numbers count and display like a graph (Histogram)</em></h2>
<ul>
<li>Create a numbers list that contains some numbers and that constains duplicates</li>
<li>Display the list</li>
<li>Display the counts of each number</li>
<li>Display number and @ symbol for each occurance</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">8</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"List contain :"</span><span class="token punctuation">,</span> numbers<span class="token punctuation">)</span>
histo <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> numbers<span class="token punctuation">:</span>
   histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Histogram of the list"</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"---------------------"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> histo<span class="token punctuation">:</span>
  <span class="token keyword">print</span><span class="token punctuation">(</span>key<span class="token punctuation">,</span> <span class="token string">"@"</span><span class="token operator">*</span>histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">List contain : [2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
Histogram of the list
---------------------
2 @
4 @@
5 @
1 @@
6 @
7 @@
8 @
3 @@
</code></pre>
<h2 id="step-4--lets-try-with-some-random-numbers-using-random-class-histogram">Step 4 : <em>Lets try with some random numbers using random class (Histogram)</em></h2>
<ul>
<li>Create a numbers list that contains random values that has lower and upper bounds for count and values.</li>
<li>Display the list</li>
<li>Display the counts of each number</li>
<li>Display number and @ symbol for each occurance</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
<span class="token keyword">import</span> random

<span class="token comment">#Values used for random functions</span>
mincount <span class="token operator">=</span> <span class="token number">20</span>
maxcount <span class="token operator">=</span> <span class="token number">200</span>
minvalue <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">10</span>
maxvalue <span class="token operator">=</span> <span class="token number">15</span>

<span class="token comment">#Source list</span>
numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>

<span class="token comment">#Random size is computed</span>
size_of_list <span class="token operator">=</span> random<span class="token punctuation">.</span>randint<span class="token punctuation">(</span>mincount<span class="token punctuation">,</span>maxcount<span class="token punctuation">)</span>

<span class="token comment">#List of random number is generated</span>

<span class="token keyword">for</span> i <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>size_of_list<span class="token punctuation">)</span><span class="token punctuation">:</span>
   numbers<span class="token punctuation">.</span>append<span class="token punctuation">(</span>random<span class="token punctuation">.</span>randrange<span class="token punctuation">(</span>minvalue<span class="token punctuation">,</span>maxvalue<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"List contain :"</span><span class="token punctuation">,</span> numbers<span class="token punctuation">)</span>
histo <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> numbers<span class="token punctuation">:</span>
   histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Histogram of the list"</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"---------------------"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> histo<span class="token punctuation">:</span>
   <span class="token keyword">print</span><span class="token punctuation">(</span>f<span class="token string">"{key:2}"</span><span class="token punctuation">,</span> <span class="token string">"@"</span><span class="token operator">*</span>histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">List contain : [6, -10, -7, -7, -4, 2, 11, 3, -3, 12, 0, -6, 14, -7, 13, -8, -5, -5, 12, -4, 1, 15, 9, 7, 11, 15, 1, 2, 6, 9, -8, 10, 2, -8, 15, -2, -6, 7, 0, 4, 10, 2, -3, 1, 4, -9, 4, 14, -7, -4, 3, -2, -7, 3, -9, 10, 10, 5, -9, 7, -9, -6, 13, -1, 8, -10, 13, 9, 4, 5, 3, -2, -2, 11, -3, -3, -2, -7, 8, 7, 13, 13, -8, 2, 0, 1, 6, -5, 1, 13, 14, 4, -3, 15, 15, 14, -3, -5, -2, 7, 4, 9, -5, -6, 13, 10, -3, 5, -5, 14, 13, 14, -9, 9, -7, 15, 6, 13, 2, 14, 4, 8, 7, -3, 15, 13, 6, 3, -5, -8, 10, -7, -3, 13, 5, 3, 13, -4, -6, 0, -2, -9, 12, 5, 10, 8, -1, 10, 3, 1, -3, 4, 1, 2, 15, 6, 6, 0, 4, 11, -8, -2, 7, 10, -3, -1, 6, 1, 0, -6, 10, 8, 6, 2, -4, -1, -4, 12, -1, 6, 13, 11, 6, -7, 4, 13, 1, -6, -2, -2, -10, 10, 6, -3, 14]
Histogram of the list
---------------------
 6 @@@@@@@@@@@@
-10 @@@
-7 @@@@@@@@@
-4 @@@@@@
 2 @@@@@@@@
11 @@@@@
 3 @@@@@@@
-3 @@@@@@@@@@@@
12 @@@@
 0 @@@@@@
-6 @@@@@@@
14 @@@@@@@@
13 @@@@@@@@@@@@@@
-8 @@@@@@
-5 @@@@@@@
 1 @@@@@@@@@
15 @@@@@@@@
 9 @@@@@
 7 @@@@@@@
10 @@@@@@@@@@@
-2 @@@@@@@@@@
 4 @@@@@@@@@@
-9 @@@@@@
 5 @@@@@
-1 @@@@@
 8 @@@@@
</code></pre>
<h2 id="step-5-lets-try-with-some-random-numbers-using-random-class-histogram-but-ordered-based-on-key">Step 5: <em>Lets try with some random numbers using random class (Histogram) but ordered (based on key)</em></h2>
<ul>
<li>Create a numbers list that contains random values that has lower and upper bounds for count and values.</li>
<li>Display the list</li>
<li>Display the counts of each number</li>
<li>Sort tupple based on the key</li>
<li>Display number and @ symbol for each occurance</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
<span class="token keyword">import</span> random

<span class="token comment">#Values used for random functions</span>
mincount <span class="token operator">=</span> <span class="token number">20</span>
maxcount <span class="token operator">=</span> <span class="token number">200</span>
minvalue <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">10</span>
maxvalue <span class="token operator">=</span> <span class="token number">15</span>

<span class="token comment">#Source list</span>
numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>

<span class="token comment">#Random size is computed</span>
size_of_list <span class="token operator">=</span> random<span class="token punctuation">.</span>randint<span class="token punctuation">(</span>mincount<span class="token punctuation">,</span>maxcount<span class="token punctuation">)</span>

<span class="token comment">#List of random number is generated</span>

<span class="token keyword">for</span> i <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>size_of_list<span class="token punctuation">)</span><span class="token punctuation">:</span>
   numbers<span class="token punctuation">.</span>append<span class="token punctuation">(</span>random<span class="token punctuation">.</span>randrange<span class="token punctuation">(</span>minvalue<span class="token punctuation">,</span>maxvalue<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"List contain :"</span><span class="token punctuation">,</span> numbers<span class="token punctuation">)</span>
histo <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> numbers<span class="token punctuation">:</span>
   histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

histo_order <span class="token operator">=</span> <span class="token builtin">sorted</span><span class="token punctuation">(</span>histo<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Ordered Histogram of the list"</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"---------------------"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>key<span class="token punctuation">,</span>value<span class="token punctuation">)</span> <span class="token keyword">in</span> histo_order<span class="token punctuation">:</span>
   <span class="token keyword">print</span><span class="token punctuation">(</span>f<span class="token string">"{key:2}"</span><span class="token punctuation">,</span> <span class="token string">"@"</span><span class="token operator">*</span>value<span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">List contain : [7, 14, -2, -8, 0, 5, 8, 3, 12, 9, 15, 0, 6, 14, 12, -6, -7, 13, 14, -2, 1, 13, -8, 11, -4, 4, -8, 6, -10, 11, -5, -7, 7, 8, -2, 1, -9, -7, 11, 14, 3, 7, -3, 10, 8, 13, 10, 3, -3, -5, 12, -6, 15, 15, 8, 5, 15, 13, -2, 2, 7, -3, -7, -4, 10, 11, 3, -1, 4, -1, 5, 15, 13, 15, -1, 15, 15, 13, -3, -10, 2, -4, -7, 4, -2, 0, 15, 7, -8, -6, 15, -9, -2, 13, 0, 9, -8, 10, 7, -9, 8, -5, 10, 14, 2, 2, 9, 7, 14, -5, -4, 11, -4, -2, 4, 2, 9, -7, 14, 14, -8, 12, 2, 12, 14, -2, 9, -10, 10, 15, 3, 11, 9, 15, -8, 3, -1, -9, 9, -6]
Ordered Histogram of the list
---------------------
-10 @@@
-9 @@@@
-8 @@@@@@@
-7 @@@@@@
-6 @@@@
-5 @@@@
-4 @@@@@
-3 @@@@
-2 @@@@@@@@
-1 @@@@
 0 @@@@
 1 @@
 2 @@@@@@
 3 @@@@@@
 4 @@@@
 5 @@@
 6 @@
 7 @@@@@@@
 8 @@@@@
 9 @@@@@@@
10 @@@@@@
11 @@@@@@
12 @@@@@
13 @@@@@@@
14 @@@@@@@@@
15 @@@@@@@@@@@@
</code></pre>
<h2 id="step-6-lets-try-with-some-random-numbers-using-random-class-histogram-but-ordered-based-on-value">Step 6: <em>Lets try with some random numbers using random class (Histogram) but ordered (based on value)</em></h2>
<ul>
<li>Create a numbers list that contains random values that has lower and upper bounds for count and values.</li>
<li>Display the list</li>
<li>Display the counts of each number</li>
<li>Reverse key and values</li>
<li>Sort tupple based on the value</li>
<li>Display number and @ symbol for each occurance</li>
</ul>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
<span class="token keyword">import</span> random

<span class="token comment">#Values used for random functions</span>
mincount <span class="token operator">=</span> <span class="token number">20</span>
maxcount <span class="token operator">=</span> <span class="token number">200</span>
minvalue <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">10</span>
maxvalue <span class="token operator">=</span> <span class="token number">15</span>

<span class="token comment">#Source list</span>
numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>

<span class="token comment">#Random size is computed</span>
size_of_list <span class="token operator">=</span> random<span class="token punctuation">.</span>randint<span class="token punctuation">(</span>mincount<span class="token punctuation">,</span>maxcount<span class="token punctuation">)</span>

<span class="token comment">#List of random number is generated</span>

<span class="token keyword">for</span> i <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>size_of_list<span class="token punctuation">)</span><span class="token punctuation">:</span>
   numbers<span class="token punctuation">.</span>append<span class="token punctuation">(</span>random<span class="token punctuation">.</span>randrange<span class="token punctuation">(</span>minvalue<span class="token punctuation">,</span>maxvalue<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"List contain :"</span><span class="token punctuation">,</span> numbers<span class="token punctuation">)</span>
histo <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> key <span class="token keyword">in</span> numbers<span class="token punctuation">:</span>
   histo<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

<span class="token comment">#dictionary items retured as key value tupples </span>
histo_tupples <span class="token operator">=</span> histo<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span>

<span class="token comment">#constructing reverse tupple list</span>
r_histo_tupples <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
<span class="token keyword">for</span> key<span class="token punctuation">,</span>value <span class="token keyword">in</span> histo_tupples<span class="token punctuation">:</span>
   r_histo_tupples<span class="token punctuation">.</span>append<span class="token punctuation">(</span><span class="token punctuation">(</span>value<span class="token punctuation">,</span>key<span class="token punctuation">)</span><span class="token punctuation">)</span>

<span class="token comment">#sorting based on vales</span>
histo_order <span class="token operator">=</span> <span class="token builtin">sorted</span><span class="token punctuation">(</span>r_histo_tupples<span class="token punctuation">,</span>reverse<span class="token operator">=</span><span class="token boolean">True</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Ordered Histogram of the list"</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"-----------------------------"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>key<span class="token punctuation">,</span>value<span class="token punctuation">)</span> <span class="token keyword">in</span> histo_order<span class="token punctuation">:</span>
   <span class="token keyword">print</span><span class="token punctuation">(</span>f<span class="token string">"{value:2}"</span><span class="token punctuation">,</span> <span class="token string">"@"</span><span class="token operator">*</span>key<span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">List contain : [-10, 12, 8, -3, 6, 8, -3, 13, -10, -10, 15, -4, -7, 11, -8, 3, 1, 4, 7, 2, 2, -7, 2, -6, 12, 4, 1, 4, 14, 2, 14, 7, 4, -9, 5, 8, 15, 15, 5, -9, -3, -10, 3, 9, -10, 7, 2, -10, -5, 4, -10, 14, 2, -5, 8, 10, 4, 15, 10, 5, 10, 3, 0, -6, 13, -9, 10, 10, -8, -1, 4, -7, 6, -1, 4, -8, 0, 15, 13, 15, -5, 2, -5, 6, -1, -5, -3, 8, -6, -2, 2, -9, 15, 4, 3, 0, -8, 15, -5, -8, 12, -1, -2, -4, 7, -5, -9, -2, -9, 15, 4, -7, -9, -7, -9, 6, 1, 8, 6, 5, 11, 13, -9, 8, 15, 1, -7, 3, -8, -7, 7, -1, -6, 6, 4, -4, 2, 15, -3, -10, 10, 8, 5, 2, 9, -4, 0, -8, -2, 3, -8, -7, 5, 10, -5, -4, 8, -9, 5, 6, 6, 12, 4, 11, 5, 6, -6, 12, 6, -3, 9, 1, 12, -7, -4, 5, -8, 6, -5, -7, -9, 11, 4, -8, 13, -1, 12, -7, 0, 15, -10, 10]
Ordered Histogram of the list
-----------------------------
 4 @@@@@@@@@@@@@
15 @@@@@@@@@@@@
 6 @@@@@@@@@@@
-7 @@@@@@@@@@@
-9 @@@@@@@@@@@
 2 @@@@@@@@@@
-8 @@@@@@@@@@
 8 @@@@@@@@@
 5 @@@@@@@@@
-5 @@@@@@@@@
-10 @@@@@@@@@
10 @@@@@@@@
12 @@@@@@@
 3 @@@@@@
-1 @@@@@@
-3 @@@@@@
-4 @@@@@@
13 @@@@@
 7 @@@@@
 1 @@@@@
 0 @@@@@
-6 @@@@@
11 @@@@
-2 @@@@
14 @@@
 9 @@@
</code></pre>
<h1 id="cyber-dojo">Cyber dojo</h1>
<p><a href="https://cyber-dojo.org/review/show/QLPTrk?was_index=33&amp;now_index=34&amp;filename=undefined">Final Solution</a></p>
<h1 id="function-based">Function Based</h1>
<h2 id="program-1">Program 1</h2>
<p><strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment">################################</span>
<span class="token comment"># Program No 1</span>
<span class="token comment"># using dictionary to build the histogram</span>
<span class="token comment">#   - using a randomizer for input</span>
<span class="token comment">#   - functionally decomposing the logic </span>
<span class="token comment">#</span>
<span class="token comment">#################################</span>
<span class="token comment"># Build a histogram</span>

<span class="token keyword">import</span> random
<span class="token comment"># build a random list </span>
<span class="token comment"># returns a list containing numbers 1 &lt;= n &lt;= maxval</span>
<span class="token comment"># the list will contain n elements where</span>
<span class="token comment">#   mincount &lt; n &lt; maxcount </span>
<span class="token keyword">def</span> <span class="token function">random_list</span><span class="token punctuation">(</span>mincount<span class="token punctuation">,</span> maxcount<span class="token punctuation">,</span> maxval<span class="token punctuation">,</span> minval<span class="token operator">=</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">:</span> 
  size <span class="token operator">=</span> random<span class="token punctuation">.</span>randint<span class="token punctuation">(</span>mincount<span class="token punctuation">,</span> maxcount<span class="token punctuation">)</span>
  alist <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
  <span class="token keyword">for</span> _ <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>size<span class="token punctuation">)</span><span class="token punctuation">:</span>
    alist<span class="token punctuation">.</span>append<span class="token punctuation">(</span>random<span class="token punctuation">.</span>randrange<span class="token punctuation">(</span>minval<span class="token punctuation">,</span> maxval<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span>		
  <span class="token keyword">return</span> alist

arlist <span class="token operator">=</span> random_list<span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">,</span> <span class="token number">120</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">,</span> <span class="token operator">-</span><span class="token number">10</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"A random list"</span><span class="token punctuation">,</span> arlist<span class="token punctuation">)</span>


<span class="token comment"># returns a list containing tuples with </span>
<span class="token comment"># value and frequency, aka a histogram</span>
<span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
<span class="token keyword">def</span> <span class="token function">generate_histogram</span><span class="token punctuation">(</span>arlist<span class="token punctuation">)</span><span class="token punctuation">:</span>
  counters <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span> <span class="token comment">#inits value to 0</span>
  <span class="token keyword">for</span> number <span class="token keyword">in</span> arlist<span class="token punctuation">:</span>
	  counters<span class="token punctuation">[</span>number<span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

  histogram <span class="token operator">=</span> <span class="token builtin">sorted</span><span class="token punctuation">(</span>counters<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token keyword">return</span> histogram

histo <span class="token operator">=</span> generate_histogram<span class="token punctuation">(</span>arlist<span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"A histogram with"</span><span class="token punctuation">,</span> histo<span class="token punctuation">)</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Visualizing the histogram"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> i <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span><span class="token builtin">len</span><span class="token punctuation">(</span>histo<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">:</span> 
  <span class="token keyword">print</span> <span class="token punctuation">(</span>f<span class="token string">'{histo[i][0]:2}'</span><span class="token punctuation">,</span> <span class="token string">'@'</span><span class="token operator">*</span>histo<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">A random list [-10, 7, 20, 8, 16, 0, 9, 15, -6, 16, 14, 6, 7, -6, 20, 17, 17, -1, -10, 1, -2, 2, -9, 20, 17, -6, 12, 0, -4, 20, 8, 4, 16, 8, -3, 9, 17, 13, 0, 9, 12, 17, -4, 9, 17, 9, 3, 12, 10, -1, -8, 5, 11, -9, 12, -6, 13, 7, 6, 17, 18, 20, 13, -1, -1, -1, 9, -2, -8, 15, 6, 11, 3, -4, 9, -8, 12, -8, 5, 19, 6, 4, 4, 5, 2, 10, 5, -6, 10, 20, -3, 1, 5, 5, 20, 2, 2, -2, 5, 16, 6, -6, -4, 3, -5, 16, -5, 16, 17, 13, -7, -8, 19, -8, 1, 20, -3]
A histogram with [(-10, 2), (-9, 2), (-8, 6), (-7, 1), (-6, 6), (-5, 2), (-4, 4), (-3, 3), (-2, 3), (-1, 5), (0, 3), (1, 3), (2, 4), (3, 3), (4, 3), (5, 7), (6, 5), (7, 3), (8, 3), (9, 7), (10, 3), (11, 2), (12, 5), (13, 4), (14, 1), (15, 2), (16, 6), (17, 8), (18, 1), (19, 2), (20, 8)]
Visualizing the histogram
-10 @@
-9 @@
-8 @@@@@@
-7 @
-6 @@@@@@
-5 @@
-4 @@@@
-3 @@@
-2 @@@
-1 @@@@@
 0 @@@
 1 @@@
 2 @@@@
 3 @@@
 4 @@@
 5 @@@@@@@
 6 @@@@@
 7 @@@
 8 @@@
 9 @@@@@@@
10 @@@
11 @@
12 @@@@@
13 @@@@
14 @
15 @@
16 @@@@@@
17 @@@@@@@@
18 @
19 @@
20 @@@@@@@@
</code></pre>
<h2 id="program-2">Program 2</h2>
<p>A histogram contains bins (lower bound, upper bound), and statistical values are dropped into these bins. Eventually, the histogram is visualized based on the bin counts. This type of histogram is what is used in more statistical analysis.<br>
<strong>Code</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment">################################</span>
<span class="token comment"># Program No 5</span>
<span class="token comment"># using tuple as key in a dictionary </span>
<span class="token comment"># to build bins of values for </span>
<span class="token comment"># visualization </span>
<span class="token comment">#</span>
<span class="token comment"># Refer https://datavizcatalogue.com/methods/histogram.html </span>
<span class="token comment">#</span>
<span class="token comment">#################################</span>
<span class="token comment"># Build a histogram</span>

<span class="token keyword">import</span> random
<span class="token comment"># build a random list </span>
<span class="token comment"># returns a list containing numbers 1 &lt;= n &lt;= maxval</span>
<span class="token comment"># the list will contain n elements where</span>
<span class="token comment">#   mincount &lt; n &lt; maxcount </span>
<span class="token keyword">def</span> <span class="token function">random_list</span><span class="token punctuation">(</span>mincount<span class="token punctuation">,</span> maxcount<span class="token punctuation">,</span> maxval<span class="token punctuation">,</span> minval<span class="token operator">=</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">:</span> 
  size <span class="token operator">=</span> random<span class="token punctuation">.</span>randint<span class="token punctuation">(</span>mincount<span class="token punctuation">,</span> maxcount<span class="token punctuation">)</span>
  alist <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
  <span class="token keyword">for</span> _ <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>size<span class="token punctuation">)</span><span class="token punctuation">:</span>
    alist<span class="token punctuation">.</span>append<span class="token punctuation">(</span>random<span class="token punctuation">.</span>randrange<span class="token punctuation">(</span>minval<span class="token punctuation">,</span> maxval<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">)</span>		
  <span class="token keyword">return</span> alist

maxval<span class="token punctuation">,</span> minval <span class="token operator">=</span> <span class="token number">100</span><span class="token punctuation">,</span> <span class="token number">10</span>
arlist <span class="token operator">=</span> random_list<span class="token punctuation">(</span><span class="token number">40</span><span class="token punctuation">,</span> <span class="token number">200</span><span class="token punctuation">,</span> maxval<span class="token punctuation">,</span> minval<span class="token punctuation">)</span>
<span class="token comment">#print("A random list", arlist)</span>

<span class="token comment"># returns a list containing tuples with </span>
<span class="token comment"># value and frequency, aka a histogram</span>
<span class="token keyword">from</span> collections <span class="token keyword">import</span> defaultdict
<span class="token keyword">def</span> <span class="token function">generate_histogram</span><span class="token punctuation">(</span>arlist<span class="token punctuation">)</span><span class="token punctuation">:</span>
  counters <span class="token operator">=</span> defaultdict<span class="token punctuation">(</span><span class="token builtin">int</span><span class="token punctuation">)</span> <span class="token comment">#inits value to 0</span>

  bincount <span class="token operator">=</span> <span class="token number">10</span>
  binwidth <span class="token operator">=</span> <span class="token punctuation">(</span>maxval<span class="token operator">-</span>minval<span class="token punctuation">)</span><span class="token operator">/</span>bincount
  <span class="token comment">#minval = min(arlist)</span>
  <span class="token comment">#maxval = max(arlist)</span>
  points <span class="token operator">=</span> <span class="token punctuation">[</span>p <span class="token keyword">for</span> p <span class="token keyword">in</span> <span class="token builtin">range</span><span class="token punctuation">(</span>minval<span class="token punctuation">,</span> maxval<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token builtin">int</span><span class="token punctuation">(</span>binwidth<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">]</span>
  
  bins <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">(</span>start<span class="token punctuation">,</span> end<span class="token number">-1</span><span class="token punctuation">)</span> <span class="token keyword">if</span> end <span class="token operator">!=</span> maxval <span class="token keyword">else</span> <span class="token punctuation">(</span>start<span class="token punctuation">,</span> end<span class="token punctuation">)</span> \
          <span class="token keyword">for</span> <span class="token punctuation">(</span>start<span class="token punctuation">,</span> end<span class="token punctuation">)</span> <span class="token keyword">in</span> <span class="token builtin">zip</span><span class="token punctuation">(</span>points<span class="token punctuation">,</span> points<span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">:</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
	<span class="token comment">#bins.append(points[-1])</span>
  
  <span class="token keyword">for</span> number <span class="token keyword">in</span> arlist<span class="token punctuation">:</span>
    <span class="token keyword">for</span> start<span class="token punctuation">,</span> end <span class="token keyword">in</span> bins<span class="token punctuation">:</span> 
      <span class="token keyword">if</span> start <span class="token operator">&lt;=</span> number <span class="token operator">&lt;=</span> end<span class="token punctuation">:</span> 
        counters<span class="token punctuation">[</span><span class="token punctuation">(</span>start<span class="token punctuation">,</span> end<span class="token punctuation">)</span><span class="token punctuation">]</span> <span class="token operator">+=</span> <span class="token number">1</span>

  <span class="token keyword">return</span> counters 

histo <span class="token operator">=</span> generate_histogram<span class="token punctuation">(</span>arlist<span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"A histogram with"</span><span class="token punctuation">,</span> histo<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Visualizing the histogram"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> <span class="token builtin">bin</span> <span class="token keyword">in</span> histo<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> 
  <span class="token keyword">print</span> <span class="token punctuation">(</span>f<span class="token string">'{str(bin[0]):&gt;10}'</span><span class="token punctuation">,</span> <span class="token string">'@'</span><span class="token operator">*</span><span class="token builtin">bin</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">)</span>

<span class="token comment"># Ordered histogram </span>
o_histogram <span class="token operator">=</span> <span class="token builtin">sorted</span><span class="token punctuation">(</span>
	<span class="token punctuation">[</span><span class="token punctuation">(</span>v<span class="token punctuation">,</span> k<span class="token punctuation">)</span> <span class="token keyword">for</span> k<span class="token punctuation">,</span> v <span class="token keyword">in</span> histo<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">,</span> reverse<span class="token operator">=</span><span class="token boolean">True</span>
<span class="token punctuation">)</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Visualizing the ordered histogram"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span> <span class="token builtin">bin</span> <span class="token keyword">in</span> o_histogram<span class="token punctuation">:</span>
  <span class="token keyword">print</span> <span class="token punctuation">(</span>f<span class="token string">'{str(bin[1]):&gt;10}'</span><span class="token punctuation">,</span> <span class="token string">'@'</span><span class="token operator">*</span><span class="token builtin">bin</span><span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
</code></pre>
<p><strong>Output</strong></p>
<pre class=" language-shell"><code class="prism  language-shell">A histogram with dict_items([((91, 100), 15), ((64, 72), 13), ((37, 45), 19), ((55, 63), 9), ((82, 90), 13), ((10, 18), 14), ((46, 54), 13), ((73, 81), 12), ((19, 27), 12), ((28, 36), 11)])
Visualizing the histogram
 (91, 100) @@@@@@@@@@@@@@@
  (64, 72) @@@@@@@@@@@@@
  (37, 45) @@@@@@@@@@@@@@@@@@@
  (55, 63) @@@@@@@@@
  (82, 90) @@@@@@@@@@@@@
  (10, 18) @@@@@@@@@@@@@@
  (46, 54) @@@@@@@@@@@@@
  (73, 81) @@@@@@@@@@@@
  (19, 27) @@@@@@@@@@@@
  (28, 36) @@@@@@@@@@@
Visualizing the ordered histogram
  (37, 45) @@@@@@@@@@@@@@@@@@@
 (91, 100) @@@@@@@@@@@@@@@
  (10, 18) @@@@@@@@@@@@@@
  (82, 90) @@@@@@@@@@@@@
  (64, 72) @@@@@@@@@@@@@
  (46, 54) @@@@@@@@@@@@@
  (73, 81) @@@@@@@@@@@@
  (19, 27) @@@@@@@@@@@@
  (28, 36) @@@@@@@@@@@
  (55, 63) @@@@@@@@@

</code></pre>

