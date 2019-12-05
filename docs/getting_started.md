---
id: getting-started
title: Getting started
---

## Quick Start

Install contract framework and private blockchain

Truffle and Ganache can be installed as a node module.

```
$ npm install -g truffle
```

```
$ npm install -g ganache-cli
```

```
git clone https://github.com/gitfunded/gitfunded-web
```

### Test, compile and deploy the contract

```
 $ cd gitfunded/gitfunded-web/truffle-contracts
 $ truffle test --network development
 $ truffle migrate --network development
```

### Start the client application

Install the node dependencies.

```
yarn install
```

Run the app in the development mode.

```
cd gitfunded/gitfunded-web/client
yarn start
```

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.


Finally, the build for the production can also be generated 

```
yarn build
```
