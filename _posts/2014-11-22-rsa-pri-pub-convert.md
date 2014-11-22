---
layout: post
title: RSA公钥私钥生成及格式转换 
category: 加密
date: 2014-11-22 21:45
tags: [加密, RSA]
---

####生成RSA密钥对

```bash
$ openssl req -x509 -out public_key.der -outform der -new -newkey rsa:1024 -keyout private_key.pem 
```

####导出pem格式的公钥

```bash
$ openssl rsa -in private_key.pem -pubout -out public_key.pem 
```

####导出不加密的pkcs8格式的私钥

```bash
$ openssl pkcs8 -topk8 -nocrypt -in private_key.pem -outform der -out private_key.der
```
