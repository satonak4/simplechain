## Hash Rate

2019/02/04更新

1060: 200 kHashes/s

1080: 300 kHashes/s

1080ti: 500 kHashes/s

# Instruction

## Windows程序

下载地址 https://github.com/satonak4/simplechain/releases/download/v0.1/win32.zip 并解压缩

### 直接运行

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

## Ubuntu

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

4. 启动miner

```
tar zxvf miner.tar.gz

cd miner

LD_LIBRARY_PATH=. ./plumber
```

### 矿池模式 (未充分测试）

1. 下载 miner

```
wget https://github.com/satonak4/simplechain/releases/download/v0.1/miner.tar.gz
```

2. 启动miner

```
tar zxvf miner.tar.gz

cd miner

LD_LIBRARY_PATH=. ./plumber -addr="127.0.0.1:8888"
```

将127.0.0.1:8888改成矿池地址
