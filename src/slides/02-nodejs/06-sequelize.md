## Sequelize

<div style="display:flex;">
<div style="flex:1">
<pre><code class="js">
// service/db.js
const Sequelize = require("sequelize")

const postgres = new Sequelize(
	"dbname","username","password",
	{
		logging: false,
		host: "host",
		port: 5432,
		dialect: "postgres",
		operatorsAliases: false,
		pool: {
			max: 100,
			min: 0,
			acquire: 30000,
			idle: 10000
		}
	}
)

</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">

postgres
	.authenticate()
	.then(() => {
		console.log("Connected")
	})
	.catch(err => {
		console.error("Connection error", err)
	})

module.exports = postgres
</code></pre>
</div>
</div>
