# external-adapter-feeds  

Description  
This application enables to access all datafeed sources via single server(express.js)  

Pre-Requisites  
npm version 8.15.0  
node version 15.14.0  
pm2 process manager  
plugin node up and running  
xdc pay chrome extension  


Steps to use external-adapter-feeds  
  
Step 1:  
Clone the repository from git to HOME folder on server where plugin node is running.  
git clone "https://github.com/GoPlugin/external-adapter-feeds.git"  
  
Step 2:  
On terminal navigate to external-adapter-feeds folder and install node modules.  
cd external-adapter-feeds  
npm install  
  
Step 3:  
Create a ".env" file and save your teejlab api key in below format(use same variable names as mentioned below).  
API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX  

Step 4:  
Add the API url's for each provider in .env file (use same variable names as mentioned below).  
BINANCE_TL_URL="teej lab binance api url"  
CRYPTOCOMPARE_TL_URL="teej lab cryptocompare api url"  
COINCAP_TL_URL="teej lab coincap api url"  
COINGECKO_TL_URL="teej lab coingecko api url"  
COINMARKETCAP_TL_URL="teej lab coinmarketcap api url"  
COINLAYER_TL_URL="teej lab coinlayer api url"  
KUCOIN_TL_URL="teej lab kucoin api url"  
TRADERMADE_TL_URL="teej lab tradermade api url"  
ZYLALABS_TL_URL="teej lab zylalabs api url"  
  
Step 5:  
Start the server by executing below command.  
pm2 start services.js

Step 6:  
Create bridge on plugin UI for each provider with below url having same port(eg: 5001)  
http://localhost:5001/tl_binance  
http://localhost:5001/tl_cryptocompare  
http://localhost:5001/tl_coincap  
http://localhost:5001/tl_coingecko  
http://localhost:5001/tl_coinmarketcap  
http://localhost:5001/tl_coinlayer  
http://localhost:5001/tl_kucoin  
http://localhost:5001/tl_tradermade  
http://localhost:5001/tl_zylalabs  - for commodities  

Step 7:  
Create jobs with above bridges for price feeds from different sources.  








