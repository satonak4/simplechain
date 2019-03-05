## Hash Rate

2019/03/05更新

1060: 410 kHashes/s

1080ti: 850 kHashes/s

# 使用说明

下载地址 https://github.com/satonak4/simplechain/releases/download/v0.2.1/win_ngpu.zip

下载后解压缩zip文件

### 双击运行方式

以文本方式打开run.bat，修改-eth后面的地址，保存退出
双击run.bat运行

### 命令行方式运行

打开命令行，进入到刚才解压缩出来的目录，运行roofer.exe，替换地址。默认接入matpool
```
roofer.exe -eth="0x83853d3d5cd1c388e0fa8cebc613216ce1ad5b71"
```
如果需要接入其它矿池，添加
```
roofer.exe -eth="0x83853d3d5cd1c388e0fa8cebc613216ce1ad5b71" -addr="sipc.matpool.io:11100"
```

### 运行错误

```diff
- 如果遇到GPU运行错误的情况，请到 https://www.geforce.cn/drivers 下载并安装最新的显卡驱动程序
```
