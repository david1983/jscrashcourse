# Express - routing

routes can be defined in external file and imported as modules

<div style="display:flex;">
<div style="flex:1">
<pre><code class="js">

// app.js
const express = require('express')
const bodyParser = require('body-parser')
const taskRouter = require('routes/task')
const app = express()
const version = "0.1"

// parse various different custom JSON types as JSON
app.use(bodyParser.json({type: 'application/json'}))

// bind the task router to the express app

app.use('/task', taskRouter)
app.get('/', (req, res) => res.json({version})

app.listen(3000)

</code></pre>
</div>
<div style="flex:1">
<pre><code class="javascript">
// routes/task.js

const express = require('express')
const router = express.Router()

// middleware that is specific to this router
router.use((req, res, next) => {
&nbsp;&nbsp;&nbsp;&nbsp;console.log('Time: ', Date.now())
&nbsp;&nbsp;&nbsp;&nbsp;next()
})

router.get('/', (req, res) => {
&nbsp;&nbsp;&nbsp;&nbsp;// get all tasks
})

router.get('/:id', (req, res) => {
&nbsp;&nbsp;&nbsp;&nbsp;const taskId = req.params.id
&nbsp;&nbsp;&nbsp;&nbsp;// get task 

})

router.post('/',(req, res) => {
&nbsp;&nbsp;&nbsp;&nbsp;const newTask = req.body
&nbsp;&nbsp;&nbsp;&nbsp;// create new task
})

module.exports = router
</code></pre>
</div>
</div>

