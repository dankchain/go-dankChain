## Install go-kekchain
When done, check [startups.md](https://github.com/dankChain/go-dankChain/blob/main/startups.md) 
Installation same as go-ethereum, forked from geth.

Clone source, and Install geth:
1) clone the repository
``` 
git clone https://github.com/dankChain/go-dankChain
```

2) set GOPATH to the local path of the repository we just cloned, add /bin 
windows requires quotes wrapped around the path, linux does not allow them...
linux:
```
export GOPATH=~/path/to/go-dankChain/bin
```
windows: 
```
export GOPATH="/c/path/to/go-dankChain/bin"
```

steps 3, and 4 starting from the root path of go-dankChain 

3) use script [mkdirbin.sh](https://github.com/bloc-Chain/go-dankChain/blob/published/mkdirbin.sh)
OR
manually make a /bin directory, and install with go 
```
mkdir bin && go install ./...
```
The bin/bin directory will contain the executables of geth

4) use the flag --danknet to initialize the genesis of mainnet dankChain, or for testnet use the flag --danktest
mainnet: 
```
--danknet
```
testnet: 
```
--danktest
```

Run geth to sync the chain (Hard coded bootnodes for auto sync.)
```
./geth --datadir walletDirName --danknet
```

Continue to startups.md
