# Source for https://launchpad.net/~freeradius/+archive/ubuntu/stable-3.0

How to build your own package:

* Create an empty working directory
 ```
mkdir ~/freeradius-custom
cd ~/freeradius-custom
 ```

* Clone this repository
 ```
apt install git devscripts equivs gdebi-core
git clone https://github.com/ubuntu-pkg/freeradius-server
 ```

* Build
 ```
cd freeradius-server
mk-build-deps -i -r
debuild binary
 ```

* Install built package
 ```
cd ..
gdebi ./*freeradius*.deb
 ```
