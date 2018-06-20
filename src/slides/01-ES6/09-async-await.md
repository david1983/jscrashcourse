# async/await
how to make async calls syncronous

<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
// ES6
async function asyncAction(idle){
    return new Promise((resolve, reject) => {
        setTimeout(function(){
                console.log("idle:" + idle)
                resolve(idle)
        },idle)
    })    
}

const result = await asyncAction(100)
console.log(result)
// 100 - after 100ms
</code></pre>
</div>
</div>
