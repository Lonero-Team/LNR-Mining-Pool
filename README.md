<img src="https://raw.githubusercontent.com/Mentors4EDU/Images/master/banner.png">

# Create a Lonero Mining Pool

### First Install Dependencies
``sudo apt-get install aptitude``\
``sudo aptitude update``\
``sudo aptitude install –with-recommends build-essential autotools-dev autoconf automake libcurl3 libcurl4-gnutls-dev git make cmake libssl-dev pkg-config libevent-dev libunbound-dev libminiupnpc-dev doxygen supervisor jq libboost-all-dev htop``\
``apt-get install build-essential libtool autotools-dev autoconf pkg-config libssl-dev``\
``apt-get install libboost-all-dev git npm nodejs nodejs-legacy libminiupnpc-dev redis-server``\
``add-apt-repository ppa:bitcoin/bitcoin``\
``apt-get update``\
``apt-get install libdb4.8-dev libdb4.8++-dev``\
``curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh``\
``bash install_nvm.sh``\
``source ~/.profile``\
``nvm install 0.10.48``\
``nvm use 0.10.48``\
``nvm alias default 0.10.48``\
``nvm use default``\
``sudo apt-get update``\
``sudo apt-get install apache2``\
``sudo ufw app list``\
``sudo ufw allow 'Apache Full'``

### Install Lonero-Beta
``git clone https://github.com/Lonero-Team/Lonero-Beta.git``\
``cd Lonero-Beta``

### Start Forknoted
``./forknoted --config-file configs/lonero.conf``

### Start Simplewallet
``./simplewallet --config-file configs/lonero.conf``

### Install Pool Software
``git clone https://github.com/forknote/cryptonote-universal-pool.git pool``\
``cd pool``\
``npm update``

### Configure Pool
``cp config_example.json config.json``\
Change ports to ``34414`` and ``34415``\
If your IP is static, change the host to your static IP.

### Start Pool
run ``node init.js ``

### Hosting the Front End
Copy files from the website to html directory:\
``sudo cp -rf admin.html config.js custom.css custom.js index.html pages/ themes/ /var/www/html ``

### Site Customization
Update your pool's IP in the configs:\
`` cd /var/www/html``\
``sudo nano config.js``\
Change the name of the pool:\
``sudo nano index.html``\
You can also update the CSS and JS files for styling and functionality as needed.

**Special thanks to:**\
The [Lonero](https://lonero.org) Website\
The [CoinWiki](https://coin.wiki) Website\
[Cryptonote Universal Pool](https://github.com/forknote/forknote-pool)
