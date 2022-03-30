# Phishing Detection on Ethereum

## ⚠ Note 
The code of Trans2vec is not included in this repository. Please download the code in [XBlock](http://xblock.pro/#/dataset/6).

## Introduction
Recently, blockchain technology has become a topic in the spotlight but also a hotbed of various cybercrimes. 
Ethereum is currently the largest blockchain platform that supports smart contracts and the corresponding cryptocurrency ether is the second-largest cyptocurrency.
Besides, among various security issues of blockchain digital cryptocurrency, the number of phishing scams accounts for more than 50% of all cybercrimes in Ethereum since 2017 and this kind of scam has become as a main threat to trading security of Ethereum, thus emerging as a serious threat to the trading security of the blockchain ecosystem. 

Our work shares phishing account information from Etherscan and the code for how to crawl it. In addition, the trans2vec algorithm for detection was also shared. 

## Dataset
### Labeled phishing account
We crawled the phishing accounts before January 3, 2019 and their first-order nodes from https://etherscan.io/accounts/label/phish-hack, and got a total of 1259 phishing accounts. We call these phishing accounts as positive examples.

### Ethereum transaction network
As 1259 addresses are labeled as phishing nodes which are the targets of the detection approach, we randomly select 1259 unlabeled nodes as the outliers. With these labeled and unlabeled nodes being the central nodes, we extract their first-order neighbors and the con- nected edges between all of them to form a subnetwork.

## Code
### The crawler code
We provide the code to crawl information from https://etherscan.io/.
### Trans2vec
We propose a novel network embedding model trans2vec specifically for transaction networks by incorporating the transaction amount values and timestamps of transaction links.
