# promises
promises are a nice way to handle concurrency


<div style="display:flex;">
<div style="flex:1">

<pre><code >
//ES5

function asyncAction(idle, cb){
    setTimeout(function(){
        console.log("idele:" + idle)
        cb()
    },idle)
}

asyncAction(100, function(){
    asyncAction(100, function(){
       // ...  welcome to callback hell    
    })    
})

</code></pre>
</div>
<div style="flex:1">

<pre><code class="javascript">
// ES6

function asyncAction(idle){
    return new Promise((resolve, reject) => {
        setTimeout(function(){
                console.log("idele:" + idle)
                resolve()
        },idle)
    })    
}

asyncAction(100)
    .then(()=> asyncAction(100))
    .then(()=> asyncAction(100))
    .then(()=> asyncAction(100))
    .catch(error => console.error(error.stack))
    .finally(()=>console.log("finished"))

</code></pre>
</div>
</div>
