# Ethereum Scam Database

*An open-source database to keep track of all the current ethereum scams*

## Usage

If you haven't already, click [here](https://nodejs.org/en/download/) to download Node.JS

- Download the latest release from [here](https://github.com/MrLuit/EtherScamDB/archive/master.zip).
- Go ahead and open a command line in the release folder
- Install all necessary packages by running ```npm install```
- Build and serve the project using `node generate.js`

Generating should take around 2 minutes the first time or after a clean, but when `_site` is already present it should only take around 2-5 seconds.

## Flags

- `--clean` Clean up all the old files and folders
- `--build` Build the project without actually serving the content
- `--serve` Serve the content in the main folder without building anything
- `--update` Update all ip addresses, nameservers and update status [May take some time]
- `--archive` Send all active domains to archive.org for caching [Takes a very long time because we don't want to flood their servers]

## Contribute

Fork this project and edit `_data/data.yaml`. Every item can have the following properties:

- **id**: A unique incremental integer
- **name**: The title of the scam, should probably not be longer than 64 characters
- **status**: The status of a scam. If `status` isn't provided and `url` is, status will be autogenerated with the `--update` flag  **(Optional)**
- **description**: A full description for the scam **(Optional)**
- **url**: The protocol + hostname for a scam website, without a trailing `/` **(Optional)**
- **category**: The category under which the item falls **(Optional)**
- **addresses**: An array of all ethereum addresses that were involved in this scam, with leading '0x'  **(Optional)**

## API

To make use of our database, the following files can be used:

- [scams.json](https://etherscamdb.info/data/scams.json)
- [addresses.json](https://etherscamdb.info/data/addresses.json)
- [ips.json](https://etherscamdb.info/data/ips.json)
- [blacklist.json](https://etherscamdb.info/data/blacklist.json)
- [whitelist.json](https://etherscamdb.info/data/whitelist.json)

## Donate

If you would like to help without contributing on GitHub yourself you can send some ETH or any other ERC20 token to [etherscamdb.eth](https://etherscan.io/address/etherscamdb.eth) :clap: