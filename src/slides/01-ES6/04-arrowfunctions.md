# arrow functions


<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
//ES5
var Person = {
    name: "Jhon",
    surname: "Doe",
    fullname: function(){
        return this.name + " " + this.surnamel
    }
}

console.log(Person.fullname())
// undefined undefined
</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// ES6
const Person = {
    name: "Jhon",
    surname: "Doe",
    fullname: () => `${this.name} ${this.surname}`
}

console.log(Person.fullname())
// Jhon Doe
</code></pre>
</div>
</div>
