## Hash Rate

1080: 240 kHashes/s

1080ti: 290 kHashes/s

## Instruction

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

### 矿池模式

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
