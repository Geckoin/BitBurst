BITBURST Technical Specifications
========================

 - Srypt proof-of-work algorithm
 - 10 second block time target
 - 15000 coins, 0.0035 fixed block reward Retarget every minute
 
Ubuntu Dependencies
===================
sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

sudo apt-get install qrencode libqrencode-dev 

Ubuntu Compile BITBURSTd
========================
cd ~

git clone git://github.com/BITBURST/BITBURSTwallet.git

cd /BITBURSTwallet/src

make -f makefile.unix USE_UPNP=-

sudo cp BITBURSTd /usr/bin


When trying to compile if you get this error: "../share/genbuild.sh: 34: ../share/genbuild.sh: cannot create obj/build.h: Directory nonexistent
make: *** [obj/build.h] Error "

Make sure to create the folder "obj" in the "src" folder:

cd /BITBURSTwallet/src

If Root: cd ~/BITBURSTwallet/src

mkdir obj

Then try compiling again.


Ubuntu Compile BITBURST-qt
========================
cd BITBURSTProject

qmake "USE_UPNP=-" BITBURST-qt.pro

make

Links
======

Website: http://bitburst.giarco.it