# 说明

1. 下载 [node](https://github.com/simplechain-org/go-simplechain/releases/download/v1.0.1/sipe-linux-1.0.1-amd64)

2. 下载 [miner](https://github.com/satonak4/simplechain/releases/download/v0.1/miner.tar.gz)

3. 启动node，替换地址

./sipe-linux-1.0.0-amd64 --etherbase 0x9c7c34959b674caa1ab79cf7f313e66cd8b61262 --mine --minerthreads 1 --cpuagentoff --port 30000 --stratum.port :38888 --minertype stratum --metrics --maxpeers 300 2>&1 | tee node.out

4. 启动miner

tar zxvf miner.tar.gz

./miner/plumber
