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
git clone https://github.com/gitfunded/contracts
git clone https://github.com/gitfunded/web
```

### Test, compile and deploy the contract

```
 $ cd gitfunded/contracts/truffle-contracts
 $ truffle test --network development
 $ truffle migrate --network development
```

### Start the client application

Install the node dependencies.

```
cd gitfunded/web
npm install
```

Run the app in the development mode.

```
cd gitfunded/web
npm start
```

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.


Finally, the build for the production can also be generated 

```
npm build
```
