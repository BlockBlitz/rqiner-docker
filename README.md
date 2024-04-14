# Rquiner Docker

***Maintinance of this container has been moved to the [BlockBlitz Miners-Docker](https://github.com/BlockBlitz/miners-docker) Repo. This repo will be deleted on or around May 14th 2024.***

This Dockerfile and run script are all you need to run rquiner locally.

***This project is not affiliated with [Qubic](http://discord.gg/qubic) or [QubicSolutions](https://qubic.solutions/). Please report any bugs related to the docker container here and miner specific bugs to the respective miner owners.***

## Usage

The following environment variables are required:
| Name           | Description                                                      | Options                                                                  | Default |
|----------------|------------------------------------------------------------------|--------------------------------------------------------------------------|---------|
| ARCHITECTURE   | System architecture for running optimized compilations of rqiner | broadwell, haswell, musl, znver2, zen2, znver3, zen3, znver4, zen4, none | none    |
| NUM_THREADS    | Number of threads to run rqminer                                 |                                                                          |         |
| WALLET_ADDRESS | Your Qubic wallet payout address                                 |                                                                          |         |
| WORKER_NAME    | Your worker name/label visible in the pool                       |                                                                          |         | 

The following command starts the rqiner container with the specified parameters

`docker run ghcr.io/BlockBlitz/rqiner:latest -e ARCHITECTIRE=none -e NUM_THREADS=my-thread-count -e WALLET_ADDRESS=my-wallet-address -e WORKER_NAME=my-worker`

Or more favorably, via the included docker-compose file.
