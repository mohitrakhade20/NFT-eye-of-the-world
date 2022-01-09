# Welcome to EYE Of The World 

To find out more about me please visit:

[📺 YouTube](https://www.youtube.com/c/MohitRakhade)

[🐦 Twitter](https://twitter.com/mohitrakhade20)

[ℹ️ linkedin](https://www.linkedin.com/in/mohit-rakhade)

# The EYE NFT minting dapp 

![alt text](https://github.com/mohitrakhade20/NFT-eye-of-the-world/blob/master/eye.jpeg?raw=true)


This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. 

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone <url_of_this_repo>
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
 "CONTRACT_ADDRESS": "0xE4be5FfFB4C68a60bd0F720cd8532Ff534528CEA",
  "SCAN_LINK": "https://mumbai.polygonscan.com/address/0xe4be5fffb4c68a60bd0f720cd8532ff534528cea#events",
  "NETWORK": {
    "NAME": "Polygon testnet",
    "SYMBOL": "Matic",
    "ID": 80001
  },
  "NFT_NAME": "Eye of the World",
  "SYMBOL": "EYE",
  "MAX_SUPPLY": 69,
  "WEI_COST": 4000000000000000000,
  "DISPLAY_COST": 4,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://testnets.opensea.io/collection/eye-of-the-world",
  "SHOW_BACKGROUND": true
}
```


```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```




```html
<title>Eye of the World</title>
<meta name="description" content="Mint your Eye of the World NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "EYE",
  "name": "Eye of the World"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.


All the code in these repos was created and explained by HashLips on the main YouTube channel.

Thanks hashlips and ali solanki for providing eye layers for this eye art