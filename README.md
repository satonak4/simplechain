## Hash Rate

2019/02/16更新

1060: 360 kHashes/s

1080: 540 kHashes/s

1080ti: 900 kHashes/s

# 使用说明

## Windows 10系统

**单卡版本** 下载地址 https://github.com/satonak4/simplechain/releases/download/v0.1/win32.zip

**多卡版本** 下载地址 https://github.com/satonak4/simplechain/releases/download/v0.2/win_ngpu.zip

下载后解压缩zip文件

### 双击运行方式

以文本方式打开run.bat，修改-eth后面的地址，保存退出
双击run.bat运行

### 命令行方式运行

打开命令行，进入到刚才解压缩出来的目录，运行roofer.exe，替换地址。默认接入matpool
```
roofer.exe -eth="0x83853d3d5cd1c388e0fa8cebc613216ce1ad5b70"
```
如果需要接入其它矿池，添加
```
roofer.exe -eth="0x83853d3d5cd1c388e0fa8cebc613216ce1ad5b70" -addr="sipc.matpool.io:11100"
```

### 运行错误

```diff
- 如果遇到GPU运行错误的情况，请到 https://www.geforce.cn/drivers 下载并安装最新的显卡驱动程序
```

## Ubuntu系统

### Solo 模式

1. 下载 node

```
wget https://github.com/simplechain-org/go-simplechain/releases/download/v1.0.1/sipe-linux-1.0.1-amd64
```

2. 启动 node，替换地址

```
chmod +x ./sipe-linux-1.0.0-amd64 && ./sipe-linux-1.0.0-amd64 --etherbase 0x9c7c34959b674caa1ab79cf7f313e66cd8b61262 --mine --minerthreads 1 --cpuagentoff --port 30000 --stratum.port :38888 --minertype stratum --metrics --maxpeers 300
```

3. 下载 miner

```
wget https://github.com/satonak4/simplechain/releases/download/v0.1/miner.tar.gz
```

4. 启动上 miner

```
tar zxvf miner.tar.gz

cd miner

LD_LIBRARY_PATH=. ./plumber
```
