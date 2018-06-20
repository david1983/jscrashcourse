# decorators
a function that modifies other functions ... but with style

<div style="display:flex;">
<div style="flex:1">
<pre><code class="javascript">
//ES5
function greet(name) {
  console.log('Hello, ' + name)
}

function loggingDecorator(wrapped) {
    // IIFE
  return function() {
    console.log('Starting')
    return wrapped.apply(this, arguments)
  }
}

const wrapped = loggingDecorator(greeting)
greet('Davide')
// Hello, Davide

wrapped('Davide')
// Starting
// Hello, Davide

</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// ES6
function leDecorator(target, propertyKey, descriptor) {
    var oldValue = descriptor.value
    descriptor.value = function() {
        console.log(`Calling "${propertyKey}" with`, arguments,target)
        let value = oldValue.apply(null, [arguments[1], arguments[0]])
        return value + "; This is awesome"
    }

        return descriptor
}

class JSMeetup {
&nbsp;&nbsp;    speaker = `Davide`
&nbsp;&nbsp;    @leDecorator
&nbsp;&nbsp;    welcome(arg1, arg2) {return `${arg1} ${arg2}`}
}

const meetup = new JSMeetup();

console.log(meetup.welcome("World", "Hello"));
</code></pre>
</div>
</div>
