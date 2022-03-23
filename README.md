# 说明
对datoms协议下的连接的coding/decoding。

## 示例

```json
var encoding = require('datoms-encoding')

var link = '6161616161616161616161616161616161616161616161616161616161616161'
var buf = encoding.decode(link)
console.log('%s -> %s', link, buf)
console.log('%s -> %s', buf, encoding.encode(buf))
```

## API

**.encoding(buf)**

**.toStr(buf)**
对buf按照‘hex’格式进行编码。
如果buf不是32bytes长度，则报错。如果buf是string,则检查是否valid并返回值。

**.decode(str)**

**.toBuf(str)**
对str解码为binary。

## License
MIT