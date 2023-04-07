---
keywords: fastai
title: previous fibonacci Using Loops
toc: false 
comments: true
categories: [java]
nb_path: _notebooks/2022-09-25-fibonaccy.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-25-fibonaccy.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-java"><pre><span></span><span class="kd">public</span> <span class="kd">class</span> <span class="nc">Fibonacci</span> <span class="p">{</span>

    <span class="kt">int</span> <span class="n">firstFib</span> <span class="o">=</span> <span class="mi">1</span><span class="p">;</span>
    <span class="kt">int</span> <span class="n">secondFib</span> <span class="o">=</span> <span class="mi">1</span><span class="p">;</span>

    <span class="kd">public</span> <span class="kt">void</span> <span class="nf">forFib</span><span class="p">(</span><span class="kt">int</span> <span class="n">numOfFib</span><span class="p">)</span> <span class="p">{</span>
        <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">==</span> <span class="mi">1</span><span class="p">)</span> <span class="p">{</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">(</span><span class="s">&quot;Using For Loop: 0&quot;</span><span class="p">);</span>
        <span class="p">}</span> <span class="k">else</span> <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">==</span> <span class="mi">2</span><span class="p">)</span> <span class="p">{</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">(</span><span class="s">&quot;Using For Loop: 0 &quot;</span> <span class="o">+</span> <span class="n">firstFib</span><span class="p">);</span>
        <span class="c1">//} </span>
        <span class="c1">//else if (numOfFib == 2) {</span>
        <span class="c1">//    System.out.println(&quot;Using For Loop: 0 &quot; + firstFib + &quot; &quot; + secondFib);</span>
        <span class="p">}</span> <span class="k">else</span> <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">&gt;</span> <span class="mi">2</span><span class="p">)</span> <span class="p">{</span>
            <span class="kt">int</span> <span class="n">prevFib</span> <span class="o">=</span> <span class="n">firstFib</span><span class="p">;</span>
            <span class="kt">int</span> <span class="n">currentFib</span> <span class="o">=</span> <span class="n">secondFib</span><span class="p">;</span>
            <span class="kt">int</span> <span class="n">nextFib</span><span class="p">;</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="s">&quot;Using For Loop: 0 &quot;</span> <span class="o">+</span> <span class="n">firstFib</span> <span class="o">+</span> <span class="s">&quot; &quot;</span> <span class="o">+</span> <span class="n">secondFib</span><span class="p">);</span>
            <span class="k">for</span> <span class="p">(</span><span class="kt">int</span> <span class="n">counter</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span> <span class="n">counter</span> <span class="o">&lt;</span> <span class="n">numOfFib</span><span class="o">-</span><span class="mi">3</span><span class="p">;</span> <span class="n">counter</span><span class="o">++</span> <span class="p">)</span> <span class="p">{</span>
                <span class="n">nextFib</span> <span class="o">=</span> <span class="n">prevFib</span> <span class="o">+</span> <span class="n">currentFib</span><span class="p">;</span> <span class="c1">// prevFib, currentFib, nextFib</span>
                <span class="n">prevFib</span> <span class="o">=</span> <span class="n">currentFib</span><span class="p">;</span>
                <span class="n">currentFib</span> <span class="o">=</span> <span class="n">nextFib</span><span class="p">;</span>
                <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="s">&quot; &quot;</span> <span class="o">+</span> <span class="n">nextFib</span><span class="p">);</span>
            <span class="p">}</span>
        <span class="p">}</span>
    <span class="p">}</span>

    <span class="kd">public</span> <span class="kt">void</span> <span class="nf">whileFib</span><span class="p">(</span><span class="kt">int</span> <span class="n">numOfFib</span><span class="p">)</span> <span class="p">{</span>
        <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">==</span> <span class="mi">1</span><span class="p">)</span> <span class="p">{</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">(</span><span class="s">&quot;Using While Loop: 0&quot;</span><span class="p">);</span>
        <span class="p">}</span> <span class="k">else</span> <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">==</span> <span class="mi">2</span><span class="p">)</span> <span class="p">{</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">(</span><span class="s">&quot;Using While Loop: 0 &quot;</span> <span class="o">+</span> <span class="n">firstFib</span><span class="p">);</span>
        <span class="c1">//} else if (numOfFib == 2) {</span>
        <span class="c1">//    System.out.println(&quot;Using While Loop: 0 &quot; + firstFib + &quot; &quot; + secondFib);</span>
        <span class="p">}</span> <span class="k">else</span> <span class="k">if</span> <span class="p">(</span><span class="n">numOfFib</span> <span class="o">&gt;</span> <span class="mi">2</span><span class="p">)</span> <span class="p">{</span>
            <span class="kt">int</span> <span class="n">prevFib</span> <span class="o">=</span> <span class="n">firstFib</span><span class="p">;</span>
            <span class="kt">int</span> <span class="n">currentFib</span> <span class="o">=</span> <span class="n">secondFib</span><span class="p">;</span>
            <span class="kt">int</span> <span class="n">nextFib</span><span class="p">;</span>
            <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="s">&quot;Using While Loop: 0 &quot;</span> <span class="o">+</span> <span class="n">firstFib</span> <span class="o">+</span> <span class="s">&quot; &quot;</span> <span class="o">+</span> <span class="n">secondFib</span><span class="p">);</span>
            <span class="kt">int</span> <span class="n">counter</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span>
            <span class="k">while</span> <span class="p">(</span><span class="n">counter</span> <span class="o">&lt;</span> <span class="n">numOfFib</span><span class="o">-</span><span class="mi">3</span><span class="p">)</span> <span class="p">{</span>
                <span class="n">nextFib</span> <span class="o">=</span> <span class="n">prevFib</span> <span class="o">+</span> <span class="n">currentFib</span><span class="p">;</span> <span class="c1">// prevFib, currentFib, nextFib</span>
                <span class="n">prevFib</span> <span class="o">=</span> <span class="n">currentFib</span><span class="p">;</span>
                <span class="n">currentFib</span> <span class="o">=</span> <span class="n">nextFib</span><span class="p">;</span>
                <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="s">&quot; &quot;</span> <span class="o">+</span> <span class="n">nextFib</span><span class="p">);</span>
                <span class="n">counter</span><span class="o">++</span><span class="p">;</span>
            <span class="p">}</span>
        <span class="p">}</span>
    <span class="p">}</span>

    <span class="kd">public</span> <span class="kt">int</span> <span class="nf">recursiveFib</span><span class="p">(</span><span class="kt">int</span> <span class="n">n</span><span class="p">)</span> <span class="p">{</span>
        <span class="k">if</span> <span class="p">(</span><span class="n">n</span> <span class="o">==</span> <span class="mi">0</span><span class="p">)</span> <span class="p">{</span>
            <span class="k">return</span> <span class="mi">0</span><span class="p">;</span>
        <span class="p">}</span> <span class="k">else</span> 
        <span class="k">if</span> <span class="p">(</span><span class="n">n</span> <span class="o">==</span> <span class="mi">1</span><span class="p">)</span> <span class="p">{</span>
            <span class="k">return</span> <span class="n">firstFib</span><span class="p">;</span>
        <span class="p">}</span> <span class="k">else</span> <span class="k">if</span> <span class="p">(</span><span class="n">n</span> <span class="o">==</span> <span class="mi">2</span><span class="p">)</span> <span class="p">{</span>
            <span class="k">return</span> <span class="n">secondFib</span><span class="p">;</span>
        <span class="p">}</span> 
        <span class="k">return</span> <span class="n">recursiveFib</span><span class="p">(</span><span class="n">n</span><span class="o">-</span><span class="mi">2</span><span class="p">)</span> <span class="o">+</span> <span class="n">recursiveFib</span><span class="p">(</span><span class="n">n</span><span class="o">-</span><span class="mi">1</span><span class="p">);</span>
        
            
        
    <span class="p">}</span>

    <span class="kd">public</span> <span class="kt">void</span> <span class="nf">printRecFib</span><span class="p">(</span><span class="kt">int</span> <span class="n">numOfFib</span><span class="p">){</span>
        <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="s">&quot;Using Recursion: &quot;</span><span class="p">);</span>
        <span class="k">for</span><span class="p">(</span><span class="kt">int</span> <span class="n">i</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="n">numOfFib</span><span class="p">;</span> <span class="n">i</span><span class="o">++</span><span class="p">){</span>
			<span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">print</span><span class="p">(</span><span class="n">recursiveFib</span><span class="p">(</span><span class="n">i</span><span class="p">)</span> <span class="o">+</span><span class="s">&quot; &quot;</span><span class="p">);</span>
		<span class="p">}</span>
    <span class="p">}</span>




    <span class="kd">public</span> <span class="kd">static</span> <span class="kt">void</span> <span class="nf">main</span><span class="p">(</span><span class="n">String</span><span class="o">[]</span> <span class="n">args</span><span class="p">)</span> <span class="p">{</span>

        <span class="n">Scanner</span> <span class="n">scanFib</span> <span class="o">=</span> <span class="k">new</span> <span class="n">Scanner</span><span class="p">(</span><span class="n">System</span><span class="p">.</span><span class="na">in</span><span class="p">);</span>
        <span class="kt">int</span> <span class="n">numOfFib</span> <span class="o">=</span> <span class="n">scanFib</span><span class="p">.</span><span class="na">nextInt</span><span class="p">();</span>
        <span class="n">Fibonacci</span> <span class="n">fibseries</span> <span class="o">=</span> <span class="k">new</span> <span class="n">Fibonacci</span><span class="p">();</span>
       
        <span class="n">fibseries</span><span class="p">.</span><span class="na">forFib</span><span class="p">(</span><span class="n">numOfFib</span><span class="p">);</span> <span class="c1">// For Loop</span>
        <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">();</span>
        <span class="n">fibseries</span><span class="p">.</span><span class="na">whileFib</span><span class="p">(</span><span class="n">numOfFib</span><span class="p">);</span> <span class="c1">// While Loop</span>
        <span class="n">System</span><span class="p">.</span><span class="na">out</span><span class="p">.</span><span class="na">println</span><span class="p">();</span>
        <span class="n">fibseries</span><span class="p">.</span><span class="na">printRecFib</span><span class="p">(</span><span class="n">numOfFib</span><span class="p">);</span> <span class="c1">// Recursive Loop</span>
        
    <span class="p">}</span>
<span class="p">}</span>

<span class="n">Fibonacci</span><span class="p">.</span><span class="na">main</span><span class="p">(</span><span class="kc">null</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Using For Loop: 0 1 1 2 3 5 8 13 21 34
Using While Loop: 0 1 1 2 3 5 8 13 21 34
Using Recursion: 0 1 1 2 3 5 8 13 21 34 </pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
