# spread operator


<div style="display:flex;">
<div style="flex:1">
<pre style="width:100%"><code class="javascript">
//ES5
var _toArray = function (arr) {
  return Array.isArray(arr) ? 
    arr : 
    [].slice.call(arr);
};

function add(a, b) {
  return a + b;
}

var nums = [5, 4];
console.log(add.apply(null, _toArray(nums)));
//9
</code></pre>
</div>
<div style="flex:1">
<pre style="width:100%"><code class="javascript">
// ES6
function add() {
  return arguments
    .reduce((accumulator, iterator) => {
        return accumulator+=iterator
    },0)
}

let nums = [5, 4];

console.log(add(...nums));
// 9
</code></pre>
</div>
</div>

