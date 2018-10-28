# [基于 Nervos AppChain 的 DApp 开发](https://learning.nervos.org/nerv-first) QA

### node-gyp安装问题

在第七章 [申请测试链代币](https://learning.nervos.org/nerv-first/7-coin)

有一个 `yarn add @nervos/chain`操作，提示

```
npm ERR! code ELiFECYCLE
npm ERR! errno 1
npm ERR! scrypt@6.0.3 install: `node-gyp rebuild`
npm ERR! Exit status 1
```

node包 scrypt 有c、c++代码，需要本地编译，node的本地编译又依赖node-gyp

在ubunut系统中：
1. 先安装本地编译的工具链

执行 `sudo apt-get install build-essential`
会安装 `make`， `gcc` 等工具。

2. 安装node-gyp

执行 `npm install node-gyp -g`
然后在执行 `yarn add @nervos/chain`即可

在Mac系统中：
略