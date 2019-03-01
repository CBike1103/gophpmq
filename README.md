# protomq

* install protoc
## php


* https://github.com/protocolbuffers/protobuf/tree/master/php

```bash
composer require google/protobuf
composer require spiral/roadrunner
```
## go

```bash
go get github.com/spiral/roadrunner
go get -u github.com/golang/protobuf/protoc-gen-go
```

## notes

```bash
panic: [5] Leader Not Available: the cluster is in the middle of a leadership election and there is currently no leader for this partition and hence it is unavailable for writes
```

## TODO

* `protomq` cli
  * 自动下载`protoc`
  * 内嵌`protomq.proto`
  * 嵌套调用`protoc`
  * protoc文件语法检查、错误提示
    * topic缺失、重复
    * proto namespace检查
    * language namespace检查
  * 消息大小限制、检查
  * 统计整合
* kafka
  * 自动控制partition？
* php
  * 支持7.X
  * 能否支持 5.x？
  * 使用context传递key？
  * go并发？
  * 控制回收？
* go
  * worker pool
* 测试
  * 大量fetch，但不commit
  * 多个group
  * 乱序commit: https://zhuanlan.zhihu.com/p/27408881
