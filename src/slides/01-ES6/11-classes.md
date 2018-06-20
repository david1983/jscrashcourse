# classes
example of how to use the prototype chain
<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
//ES5
// Initialize constructor functions
function Hero(name, level) {
  this.name = name;
  this.level = level;
}

function Warrior(name, level, weapon) {
  Hero.call(this, name, level);

  this.weapon = weapon;
}

function Healer(name, level, spell) {
  Hero.call(this, name, level);

  this.spell = spell;
}


</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// ES5
// Link prototypes and add prototype methods
Warrior.prototype = Object.create(Hero.prototype);
Healer.prototype = Object.create(Hero.prototype);

Hero.prototype.greet = function () {
  return `${this.name} says hello.`;
}

Warrior.prototype.attack = function () {
  return `${this.name} attacks with the ${this.weapon}.`;
}

Healer.prototype.heal = function () {
  return `${this.name} casts ${this.spell}.`;
}

// Initialize individual character instances
var hero1 = new Warrior('Bjorn', 1, 'axe');
var hero2 = new Healer('Kanin', 1, 'cure');

</code></pre>
</div>
</div>
