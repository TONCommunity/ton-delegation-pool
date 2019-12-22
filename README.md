# TON Delegation Pool platform
![Image of Pool](https://github.com/button-tech/ton-delegation-pool/raw/master/docs/delegation.png)


## Answers on Telegram Contest Key points

#### Describes your project and how users will interact with it 

This project allows anyone to create delegation pool and become validator. Also it allows anyone to earn interest by delegating Grams to potential Validators. (Risks will be handled by reputation system and security deposits). It is non-custodial solution, it is web based solution (all private keys and operations with it are on client side). 
 It is WEB platform features like:
 1. Cross-platform client side wallet
 2. Integrated Dapp that allows to delegate and withdraw funds without CLI

Users will interact with it in two ways. Delegators will just use web based platform or any compatible wallet. They just need to find a delegation pool and send funds to it. They can track statuses of pool via Web platform or can subscribe to the bot notification. Validators can deploy delegation pool via WEB platform. However, to ensure that everything is ok, they will need to use terminal to sign all neccesary data to stake funds from delegation pool to elector pool.

#### Explains how your code should be used to deploy and use your smart contract.


THE BEST WAY to run everything locally is use docker compose

```
docker-compose up
```

We assume that anyone who is going to run this project from scratch is familiar with: C++, Python, Angular, JS, Fift, Func, Go Bash and Zsh as well as MongDB. To run from scracth you will need light client, that will be used by contracts and by api folder. Also you need to have npm installed to build frontend.

To deploy smart contract go to: https://github.com/button-tech/ton-delegation-pool/contracts 

To run backend go to: https://github.com/button-tech/ton-delegation-pool/api

To run frontend go to: https://github.com/button-tech/ton-delegation-pool/front

It is possible to deploy smart contract via WEB frontend only. We use our own backend wrappers over light client to send Boc and run some methods.

# Video 
### Interaction with production elector smart contract (from web)
[![Alt text](https://img.youtube.com/vi/AKCNmtSnO6E/0.jpg)](https://www.youtube.com/watch?v=AKCNmtSnO6E)
### Interaction with production elector smart contract (from terminal) 
[![Alt text](https://img.youtube.com/vi/gZh2N2zzxHg/0.jpg)](https://www.youtube.com/watch?v=gZh2N2zzxHg)
### Interaction with elector smart contract (mocked for fast tests)
[![Alt text](https://img.youtube.com/vi/y9RfvadfX2c/0.jpg)](https://www.youtube.com/watch?v=y9RfvadfX2c)

# Presentation

### Availible [here](https://t.me/ton2Contest/2)

Telegram: https://t.me/ton2Contest/2

Local: [GitHub](https://github.com/button-tech/ton-delegation-pool/raw/master/docs/Delegation_dapp.pdf)

# Demo
### Try it [here](https://contest.buttonwallet.com) 


# Run and Build

fast way (use our image for run api):
```
# docker-compose up
```

full build:
```
# docker-compose -f docker-compose-full-build.yml build
# docker-compose -f docker-compose-full-build.yml up
```

Open your browser at http://127.0.0.1 - front
Open your browser at http://127.0.0.1:3000/docs - API(Swagger)

# ToDo:

- [ ] Validator fee commission
- [ ] Security deposit
- [ ] Sub delegation Charity pool and ICO pool

# 3rd party libs:

Thanks to https://github.com/EmelyanenkoK

With https://github.com/EmelyanenkoK/ValeriTon that was used as a base for web version.

We customized these library to deploy our contract and run functions on it


# Authors 

Nick Kozlov - CTO and Co-founder of BUTTON Wallet (@enormousrage, nk@buttonwallet.com)

Kirill Kuznecov - Co-founder of BUTTON Wallet (@krboktv, kk@buttonwallet.com)

Alexey Prazdnikov - Fullstack developer at BUTTON Wallet (@noprazd, ap@buttonwallet.com)


