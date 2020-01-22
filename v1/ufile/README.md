# ufile-sdk

对 UFile 官方提供 ufile-nodejssdk 进行了配置方法上的改造，可在调用 sdk 时，传入 public-key 和 private-key 等配置信息，方便安装使用。

UFfile SDK 参考下载列表： <https://docs.ucloud.cn/storage_cdn/ufile/tools/sdk>

## 用例

``` js
var HttpRequest = require('ufile-sdk').HttpRequest;
var AuthClient = require('ufile-sdk').AuthClient;
var req = new HttpRequest(method, url_path_params, bucket, key, filePath);
var options = {
  ucloud_public_key: 'config.publicKey',
  ucloud_private_key: 'config.privateKey',
  proxy_suffix: 'config.proxySuffix'
}
var client = new AuthClient(req, options);
client.SendRequest(callbackFn);
```
