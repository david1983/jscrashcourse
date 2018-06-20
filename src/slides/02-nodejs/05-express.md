# Express

Express.js, or simply Express, is a web application framework for Nodejs.

```javascript

const express = require('express')
const app = express()
const version = "0.1"

app.get('/', (req, res) => res.json({version})

app.listen(3000, () => console.log('Example app listening on port 3000!'))

```