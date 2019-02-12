UltraPayCoin (fork of PIVX) integration/staging repository
======================================


It is recommended [use the shell script](https://https://github.com/upc-dev-team//UPCinstall) to install a UltraPayCoin Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

Quick installation of the UltraPayCoin daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/upc-dev-team/UltraPayCoin.git
    cd UltraPayCoin
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip ultrapaycoind
    sudo strip ultrapaycoin-cli
    sudo strip ultrapaycoin-tx
    cd ..

Running the daemon:

    ultrapaycoind 

Stopping the daemon:

    ultrapaycoin-cli stop

Demon status:

    ultrapaycoin-cli getinfo
    ultrapaycoin-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/upc-dev-team/UltraPayCoin/releases

P2P port: 13333, RPC port: 13334
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
