#Examples

```javascript
// app.js
var qrcode = require('express-qrcode');
// ...
app.use(qrcode);
```

```javascript
//routes/index.js
var express = require('express');
var router = express.Router();

/* GET home page. */
router.get('/', function(req, res) {
    var qrcode = req.qrcode();
    qrcode.setDimension(120,120);
    qrcode.setCharset('UTF-8');
    qrcode.setCharset('UTF-8');
    qrcode.setCorrectionLevel('L',0);
    qrcode.setData("teste");
    var image = qrcode.getImage();
  res.render('index', { title: 'Express',img:image });
});

module.exports = router;
```	
