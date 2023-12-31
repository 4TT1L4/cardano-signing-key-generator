## Overview

This repository contains the code for a simple utility tool to generate random payment signing keys for the Cardano Networks.

The tool generates a recovery phrase as well, so the wallet could be easily imported into a browser extension like Eternl or any other Cardano Wallet.

![image](https://github.com/4TT1L4/cardano-signing-key-generator/assets/2914096/1ae3aeab-5480-47e7-9208-ec38255e5844)

## Usage

In order to generate a Cardano MAINNET payment signing key, use the following command:

```
docker run -it --rm ghcr.io/4tt1l4/cardano-signing-key-generator:latest
```

Payment signing keys for the PREPROD TESTNET can be generated by explicitly setting the NETWORK variable to TESTNET:

```
docker run -it -e NETWORK=testnet --rm ghcr.io/4tt1l4/cardano-signing-key-generator:latest
```

It is also possible to pass the recovery phrase to be used, instead of randomly generating a new recovery phrase.

To do so, just set the PHRASE environment variable to the recovery phrase to be used:

```
docker run -it --rm \
    -e NETWORK=testnet \
    -e PHRASE="rate second vibrant hotel picnic chaos arch scale inner antique silver lounge symbol pink accident scout verify keen curve balance expose panda sing brisk" \
    ghcr.io/4tt1l4/cardano-signing-key-generator:latest
```
