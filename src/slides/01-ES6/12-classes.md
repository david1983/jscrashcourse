# classes
previous example but with classes
<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
//ES6
// Initialize constructor functions

class Hero {
  
      constructor(name, level){
        this.name = name
        this.level = level
      }

      greet(){return `${this.name} says hello.`}
}

class Warrior extends Hero{
  
      constructor(name, level, weapon){
        super(name, level)
        this.weapon = weapon
      }

      attack(){return `${this.name} attacks with the ${this.weapon}.`}

}




</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
class Healer extends Hero{
  
      constructor(name, level, spell){
        super(name, level)
        this.spell = spell
      }

      heal(){return `${this.name} casts ${this.spell}.`}
}


// Initialize individual character instances
const hero1 = new Warrior('Bjorn', 1, 'axe');
const hero2 = new Healer('Kanin', 1, 'cure');
</code></pre>
</div>
</div>
