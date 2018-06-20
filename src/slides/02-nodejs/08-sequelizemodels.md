## Sequelize models

<div style="display:flex;">
<div style="flex:1">
<pre><code class="js">

const Task = require("models/task")

Task.findAll()
	.then(result => console.log(result))
	.catch(error => console.error(error))

Task.findById(1)
	.then(result => console.log(result))
	.catch(error => console.error(error))

Task.destroy({where:{id: 1}})
	.then(result => console.log(result))
	.catch(error => console.error(error))

</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">

Task.update({name: 'test', description:'test'}, 
			{returning: true, where:{id: 1}})
	.then(result => console.log(result))
	.catch(error => console.error(error))

Task.create({name: 'test', description:'test'})
	.then(result => console.log(result))
	.catch(error => console.error(error))

</code></pre>
</div>
</div>
