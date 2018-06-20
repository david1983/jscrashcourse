# ES6 modules


<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
// CommonJS

// somemodule.js
var someModule = {
    test: 1
}
module.exports = someModule

// main.js
var someModule = require("./somemodule")
console.log(someModule.test)

// 1
</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// ES6

// somemodule.js
var someModule = {
    test: 1
}
export default someModule

// main.js
import somemodule from "./somemodule"
console.log(someModule.test)

// 1

</code></pre>
</div>
</div>
