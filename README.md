<div align="center">
  <br />
  <br />
  <a href=""><img alt="Pessimism" src="https://raw.githubusercontent.com/ethereum-pessimism/media/f7147b15246ae829c8e628e8e851347235a00193/assets/svg/Blue%20Text.svg" width=600></a>
  <br />
  <h3><a href="">Pessimism</a> is a scalable and secure L2 pessimistic rollup chain. Pessimism is an active member of the Optimism OPstack and is contributing to the Optimism Superchain.</h3>
  <br />
</div>

> **Warning**
> Pessimism is no where to production ready. We are constantly working on our core services such as dispute mechanism, batch submitter and onchain tx engine. 

## What is Pessimsim?

Pessimism is a newly created Layer-2 chain built on top of the Optimism Stack. Pessimism provides so called pessimistic rollups for ethereum transaction. 

## Documentation

## Community

## Development Setup

1. These packages are all required either to compile the software or to run it. We need libusb-1.0 because geth requires it to check for hardware wallets.

```bash
sudo apt install -y git make wget gcc pkg-config libusb-1.0 jq
```

2. Install the node version manager which is used to dynamicall install node versions based on your needs.

```bash
curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh -o install_nvm.sh | bash
export NVM_DIR="$HOME/.nvm"
  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
  [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

3. Install node version 14.x

```bash
nvm install 14
node -v
```

4. Install yarn 

```bash
sudo npm install -g yarn 
```

5. Install golang programming-language used to compile l2geth and the pessimism node

```bash
sudo apt install golang-go
```

6. Setting up the Data Transport Layer

```bash
git clone https://github.com/ethereum-pessimism/pessimism
cd pessimism
yarn
yarn build
cd ~/pessimism/packages/data-transport-layer
cp .env.example .env
```

7. Compiling the Layer-1 geth client

```bash
cd ~/pessimism/l2geth
make geth
```

## Contributing

Read through [CONTRIBUTING.md](./CONTRIBUTING.md) for a general overview of our contribution process.
Use the [Developer Quick Start](./CONTRIBUTING.md#development-quick-start) to get your development environment set up to start working on the Pessimism Monorepo.
Then check out our list of [good first issues]() to find something fun to work on!

### Overview

We generally follow [this Git branching model](https://nvie.com/posts/a-successful-git-branching-model/).
Please read the linked post if you're planning to make frequent PRs into this repository (e.g., people working at/with Pessimism).


## License

Code forked from [`go-ethereum`](https://github.com/ethereum/go-ethereum) under the name [`l2geth`](https://github.com/ethereum-pessimism/pessimism/tree/master/l2geth) is licensed under the [GNU GPLv3](https://gist.github.com/kn9ts/cbe95340d29fc1aaeaa5dd5c059d2e60) in accordance with the [original license](https://github.com/ethereum/go-ethereum/blob/master/COPYING). Pessimism is built on top of a optimism hard-fork. MIT Optimism Foundation. Part of the Optimism Superchain and OPstack. 

All other files within this repository are licensed under the [MIT License](https://github.com/ethereum-pessimism/pessimism/blob/master/LICENSE) unless stated otherwise.
