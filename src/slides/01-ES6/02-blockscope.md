# Block scope
## const and let instead of var

<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
if(true){
    var a = true
}
console.log(a)
// true (WTF!!!)

(function(){
    test = 2
})()

// even within a clojure, if you
// declare a variable without using
// the var keyword the variale is
// stored in the global scope

console.log(test)
// 2 
</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
if(true){
    let a = true
}
console.log(a)
// a is not defined (aaah!)
const someconst = 0
someconst = 2
// Uncaught TypeError: 
// Assignment to constant variable
</code></pre>
</div>
</div>
