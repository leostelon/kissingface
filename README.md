
# Kissing Face😘

Kissing Face is a decentralized version of [Hugging Face](https://huggingface.co/)/[Kaggle](https://www.kaggle.com/), enabling you to train and test your datasets and models onsite using [Bacalhau](https://docs.bacalhau.org/), and or access wider range of datasets and models via DAO. 

![Home Page](https://kissing-face-09fc6f51-bc74-41e7-9ecf-433804ba-7ecac0.spheron.app/Screenshot_11.png)
[](https://kissingface.xyz)<center>https://kissingface.xyz</center>

> 🔴**IMPORTANT**🔴 
> 
> 1. Spheron Compute has some caching issues; recommended to run locally
> for testing purposes; please check the guide below on running it
> locally.
> 2. Use a non rate-limited RPC endpoints to avoid failures. 
> 3. And also don't interact with older datasets, create your own before testing. Thanks :)

# Get Started

The product contains three code bases, Server to serve Bacalhau commands and Client, a GUI code base, and Solidity code to manage and handle DAO. Database is handled by [Polybase](https://polybase.xyz/), a database for web3.

1. [Server](https://github.com/leostelon/kissingface-server)
2. [Client](https://github.com/leostelon/kissingface-client)
4. [Contracts](https://github.com/leostelon/kissingface-client/tree/main/src/contracts)

**Website**

[kissingface.xyz](https://kissingface.xyz/)

**API**

[API KissingFace](https://api.kissingface.xyz/)

# Accomplishments/Milestones

 - Tokenize the Dataset's using a basic blueprint, [read here](https://docs.google.com/document/d/1OYDh_gs7mAk2M_O9m-2KedQA7MNo6ysIzH6eaQZxMOk/edit?pli=1).
 - Integrating Bacalhau with node.js to serve request's through APIs.
 - Authentication for downloading dataset's and for using Bacalhau features.

# Technology
 - **Bacalhau** hosted on **Spheron Decentralized Compute** [[know more]](https://spheron.network/#decentralised-compute), served using Node.js and Express.js server through APIs.
	 - Find bacalhau and other API logics [here](https://github.com/leostelon/kissingface-server/tree/main/src/routes).
 - Database, **Polybase** is the database for web3. [[know more]](https://polybase.xyz/)
	- Find schemas and logic [here](https://github.com/leostelon/kissingface-server/tree/main/src/polybase).
- Datasets and models are stored in Decentralized storage using **Spheron Storage SDK**, [[know more]](https://spheron.network/#storage-sdk)
- React.js, hosted on **Spheron Decentralized Hosting**  [[know more]](https://spheron.network/#decentralized-hosting)

Follow the below steps to run it locally.

## Server⚙️
> ⚠️ Make sure you have installed Bacalhau Client. [Know More](https://docs.bacalhau.org/getting-started/installation)

1. Clone Repo.
> $ git clone https://github.com/leostelon/kissingface-server kissingface-server
>  $ cd kissingface-server
2. Add the .env file in the root directory. Add the below variables and replace them with your tokens, respectively.

	  SPHERON_TOKEN= < spheron-webapp-token > [Know More](https://docs.spheron.network/rest-api/#creating-an-access-token)
POLYBASE_NAMESPACE= < polybase-namespace > [Know More](https://explorer.testnet.polybase.xyz/studio)
JWT_SECRET= < your-secret >
3. Run server!
#### Run independently
> $ npm run start
#### Run using Docker🐟
> $ docker build -t kissingface:latest .

## Client💻

1. Clone Repo.
> $ git clone https://github.com/leostelon/kissingface-client kissingface-client
>  $ cd kissingface-client
2. Add the .env file in the root directory. Replace the value accordingly.

		  REACT_APP_SERVER_URL=http://localhost:3000
	  
4. Run the client!
> $ npm run start

Note: It may prompt to run on a different port, hit enter.

## What next?👨‍💻
 - [x] MVP
 - [x] Datasets
 - [x] Stable-Diffusion
 - [ ] Add support for models
