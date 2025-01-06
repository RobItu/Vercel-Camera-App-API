# Echo API Documentation

## Overview

This repository contains a serverless API endpoint hosted on [Vercel](https://vercel-camera-app-api.vercel.app/api/echo). The primary function of this API is to interact with Chainlink Functions (CLF). When CLF sends a POST request to this endpoint, the API echoes back the received data. This data is then captured by CLF and recorded on the blockchain. This mechanism ensures that data processed through this endpoint is verifiably posted on the blockchain, maintaining transparency and integrity.

## Purpose

The API serves as a crucial component in the data verification process, ensuring that any data sent to it is not only returned but also securely and transparently recorded on the blockchain. This setup is ideal for applications requiring data integrity and verifiability in blockchain operations.

## How It Works

1. **Receiving Data**: Chainlink Functions send data to this API via a POST request.
2. **Processing Data**: Upon receiving the data, the API immediately echoes this data back in the response.
3. **Blockchain Interaction**: The returned data is captured by Chainlink, which then handles the process of recording it on the blockchain.

## Deployment

The API is deployed on Vercel, which offers seamless scalability and management of serverless applications. Vercel automatically handles the scaling of the API based on request volume, ensuring efficient performance regardless of load.

## Usage

To use this API, send a POST request to the endpoint with any JSON payload. Below is an example using `curl`:

```bash
curl -X POST  https://vercel-camera-app-api.vercel.app/api/echo -H "Content-Type: application/json" -d '{"message":"hello"}'
```

### Expected Response

```bash
{
    "message": "hello"
}
```
