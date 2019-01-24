# simplechain

1. download [node binary](https://github.com/simplechain-org/go-simplechain/releases/download/v1.0.1/sipe-linux-1.0.1-amd64)

2. download latest [miner binary](https://github.com/satonak4/simplechain/releases/download/v0.1/plumber)

3. start node

./sipe-linux-1.0.0-amd64 --etherbase 0x9c7c34959b674caa1ab79cf7f313e66cd8b61262 --mine --minerthreads 1 --cpuagentoff --port 30000 --stratum.port :38888 --minertype stratum --metrics --maxpeers 300 2>&1 | tee node.out

4. start miner

./plumber
