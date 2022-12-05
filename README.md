# Lycoris

## Get started

Install [go](https://go.dev/dl/)

## Build and install to go bin path

```
make install
```

## Initialize config

Come up with a moniker for your node, then run:

```
lycorisd init $MONIKER
```
 
 
 
## Launch with genesis file or run as standalone chain

To launch as a consumer chain, download and save shared genesis file to `~/.lycoris/config/genesis.json`. Additionally add peering information (`persistent_peers` or `seeds`) to `~/.lycoris/config/config.toml`

To instead launch as a standalone, single node chain, run:

```
lycorisd add-consumer-section
```

## Launch node

```
lycorisd start
```

## NFT Module

```bash
lycorisd tx nft issue takina --mint-restricted=false --update-restricted=false --keyring-backend file --from lyco

lycorisd tx nft mint takina t001  --from lyco --keyring-backend file

lycorisd q nft collection takina

lycorisd q nft token takina t001

```
