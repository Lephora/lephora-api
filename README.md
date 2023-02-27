## Lephora Server Openapi

lephora商城后端api定义

## Development

配置hook
```shell
chmod -R +x .githooks
git config core.hooksPath .githooks
```

执行openapi定义检查
```shell
./openapi-validator lephora-server-api.yaml
```


## For CI

#### dev环境

后端推送代码时，应该以当前main分支的api定义进行spec验证，产物为测试报告，依旧可以正常的merge

#### prod环境

代码release之前，应该先tag一个对应版本的spec定义并且进行验证，产物为测试报告，测试失败时，阻止发布
