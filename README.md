# simplechain

1. download node [binary](https://www.simplechain.com/ims/chainbox/download?spm=1922.1381.010729.122&system=linux)

2. download latest miner binary from [release page](https://github.com/satonak4/simplechain/releases)

3. start node

./sipe-linux-1.0.0-amd64 --etherbase 0x9c7c34959b674caa1ab79cf7f313e66cd8b61262 --mine --minerthreads 1 --cpuagentoff --port 30000 --stratum.port :38888 --minertype stratum --metrics --maxpeers 300 2>&1 | tee node.out

4. start miner

./plumber
