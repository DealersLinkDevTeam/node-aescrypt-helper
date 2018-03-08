# node-aescrypt-helper

`node-aescrypt-helper` is a helper module that assists with the AES-256 encryption and decryption of data with arbitrary lengths.

# [Installation](#installation)
<a name="installation"></a>

```shell
npm install @dealerslink/node-aescrypt-helper
```

# [Usage](#usage)
<a name="usage"></a>

```js
const AESCryptHelper = require('@dealerslink/node-aescrypt-helper');

const secret = '41e8c08ff31f97547ac11cc47c29f8ce5cb187a70ef09226c0f025c25c55b5b3';
const iv = '3816d1474cf82f3182b83c390d3e8eb5';
const creds = { secret: null, iv: null };

creds.secret = Buffer.from(secret, 'hex');
creds.iv = Buffer.from(iv, 'hex');
const aescyptHelper = new AESCryptHelper(creds.secret, creds.iv);

console.log(aescryptHelper.decrypt(aescryptHelper.encrypt('Test Message')));
```

See wiki for more details.
