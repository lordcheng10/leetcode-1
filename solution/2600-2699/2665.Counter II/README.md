# [2665. Counter II](https://leetcode.cn/problems/counter-ii)

[English Version](/solution/2600-2699/2665.Counter%20II/README_EN.md)

## 题目描述

<!-- 这里写题目描述 -->

<p>Write a function&nbsp;<code>createCounter</code>. It should accept an initial integer&nbsp;<code>init</code>. It should return an object with three functions.</p>

<p>The three functions are:</p>

<ul>
	<li><code>increment()</code>&nbsp;increases&nbsp;the current value by 1 and then returns it.</li>
	<li><code>decrement()</code>&nbsp;reduces the current value by 1 and then returns it.</li>
	<li><code>reset()</code>&nbsp;sets the current value to&nbsp;<code>init</code>&nbsp;and then returns it.</li>
</ul>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre>
<strong>Input:</strong> init = 5, calls = [&quot;increment&quot;,&quot;reset&quot;,&quot;decrement&quot;]
<strong>Output:</strong> [6,5,4]
<strong>Explanation:</strong>
const counter = createCounter(5);
counter.increment(); // 6
counter.reset(); // 5
counter.decrement(); // 4
</pre>

<p><strong class="example">Example 2:</strong></p>

<pre>
<strong>Input:</strong> init = 0, calls = [&quot;increment&quot;,&quot;increment&quot;,&quot;decrement&quot;,&quot;reset&quot;,&quot;reset&quot;]
<strong>Output:</strong> [1,2,1,0,0]
<strong>Explanation:</strong>
const counter = createCounter(0);
counter.increment(); // 1
counter.increment(); // 2
counter.decrement(); // 1
counter.reset(); // 0
counter.reset(); // 0
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>-1000 &lt;= init &lt;= 1000</code></li>
	<li><code>total calls not to exceed 1000</code></li>
</ul>

## 解法

<!-- 这里可写通用的实现逻辑 -->

<!-- tabs:start -->

### **TypeScript**

```ts
type ReturnObj = {
    increment: () => number;
    decrement: () => number;
    reset: () => number;
};

function createCounter(init: number): ReturnObj {
    let val = init;
    return {
        increment() {
            return ++val;
        },
        decrement() {
            return --val;
        },
        reset() {
            return (val = init);
        },
    };
}

/**
 * const counter = createCounter(5)
 * counter.increment(); // 6
 * counter.reset(); // 5
 * counter.decrement(); // 4
 */
```

### **...**

```

```

<!-- tabs:end -->
