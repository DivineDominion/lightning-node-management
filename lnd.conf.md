# lnd.conf example
Based on:  
* https://github.com/lightningnetwork/lnd/blob/master/sample-lnd.conf  
* https://github.com/rootzoll/raspiblitz/blob/master/home.admin/assets/lnd.bitcoin.conf

```
# Example configuration for lnd.

[Application Options]
debuglevel=debug
maxpendingchannels=5
# up to 32 UTF-8 characters
alias=ALIAS
# choose from: https://www.color-hex.com/
color=COLOR
nat=false
minchansize=1000000
protocol.wumbo-channels=1 
accept-keysend=true
sync-freelist=true
bitcoin.feerate=100

# RPC open to all connections on Port 10009
rpclisten=0.0.0.0:10009
# REST open to all connections on Port 8080
restlisten=0.0.0.0:8080
# Domain, could use https://freedns.afraid.org
#tlsextradomain=lightning.yourhost.com  

[Bitcoin]
bitcoin.active=1
bitcoin.node=bitcoind
# enable either testnet or mainnet
#bitcoin.testnet=1
bitcoin.mainnet=1

[Bitcoind]
bitcoind.rpcuser=RPC_USER
bitcoind.rpcpass=RPC_PASSWORD
bitcoind.rpchost=127.0.0.1
bitcoind.zmqpubrawblock=tcp://*:28332
bitcoind.zmqpubrawtx=tcp://*:28333
bitcoind.estimatemode=CONSERVATIVE

[Wtclient]
wtclient.active=1

[Watchtower]
watchtower.active=1
```