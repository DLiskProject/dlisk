# DL(i)sk

DL(i)sk is a next generation crypto-currency and decentralized application platform, written entirely in JavaScript. For more information please refer to our website: https://dlisk.com/.

## Installation

**NOTE:** The following is applicable to: **Ubuntu 14.04 (LTS) - x86_64**.

Install essentials:

```
sudo apt-get update
sudo apt-get install curl build-essential python
```

Install PostgreSQL (version 9.5.2):

```
curl -sL "https://downloads.lisk.io/scripts/setup_postgresql.Linux" | bash -
sudo -u postgres createuser --createdb --password $USER
createdb dlisk_test
```

Install Node.js (version 0.12.x) + npm:

```
curl -sL https://deb.nodesource.com/setup_0.12 | sudo -E bash -
sudo apt-get install -y nodejs
```

Install grunt-cli (globally):

```
sudo npm install grunt-cli -g
```

Install bower (globally):

```
sudo npm install bower -g
```

Install node modules:

```
npm install
```

Install Dlisk Node, a specialized version of Node.js used to execute dapps within a virtual machine:

```
wget https://downloads.lisk.io/lisk-node/lisk-node-Linux-x86_64.tar.gz
tar -zxvf lisk-node-Linux-x86_64.tar.gz
```

Dlisk Node has to be in `[DLISK_DIR]/nodejs/node`.

Load git submodules ([dlisk-ui](https://github.com/DliskProject/dlisk-ui) and [dlisk-js](https://github.com/DliskProject/dlisk-js)):

```
git submodule init
git submodule update
```

Build the user-interface:

```
cd public
npm install
bower install
grunt release
```

## Launch

To launch DL(i)sk:

```
node app.js
```

**NOTE:** The **port**, **address** and **config-path** can be overridden by providing the relevant command switch:

```
node app.js -p [port] -a [address] -c [config-path]
```
## Tested on

- Ubuntu LTS 14.04
- Arch Linux
- Debian 8 "Jessie"

## Authors

- Jan West <janwest01987@gmail.com>
- Boris Povod <boris@crypti.me>
- Pavel Nekrasov <landgraf.paul@gmail.com>
- Sebastian Stupurac <stupurac.sebastian@gmail.com>
- Oliver Beddows <oliver@dlisk.io>

## License

The MIT License (MIT)

Copyright (c) 2016 DL(i)sk
Copyright (c) 2016 Lisk
Copyright (c) 2014-2015 Crypti

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:  

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
