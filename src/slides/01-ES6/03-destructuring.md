# Destructuring
destructuring allows the unpacking of values from arrays, or properties from objects, into distinct variables.


<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
// ES5
var obj = { a: 1, b: 2, c: 3}
var a = obj.a
var b = obj.b
var c = obj.c
</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// ES6
const obj = { a: 1, b: 2, c: 3}
const {a,b,c} = obj

const [d,e,f] = [1,2,3]

</code></pre>
</div>
</div>
