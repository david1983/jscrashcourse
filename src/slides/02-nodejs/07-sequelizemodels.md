## Sequelize models

<div style="display:flex;">
<div style="flex:1">
<pre><code class="js">
// models/task.js
const db = require("../services/db")
const Sequelize = require("sequelize")

const Task = sla_monitor.define(
	"task",
	{
		id: {
			type: Sequelize.BIGINT,
			primaryKey: true,
			autoIncrement: true
		},
		name: {
			type: Sequelize.TEXT,
			allowNull: false
		},
// ...


</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
		description: {
			type: Sequelize.TEXT
		},
		created_at: {
			type: Sequelize.DATE
		},
		updated_at: {
			type: Sequelize.DATE
		}
	},
	{
		schema: "sla",
		tableName: "issuers",
		timestamps: true,
		underscored: true
	}
)

module.exports = Task
</code></pre>
</div>
</div>
