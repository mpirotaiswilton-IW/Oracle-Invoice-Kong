# Oracle-Invoice-Kong

 The following repository deploys a containerized Kong API Gateway instance with an OpenAPI spec document for Oracle Financials Cloud's REST API, with endpoints specific to invoices only.

## Summary
[Oracle-Invoice-Kong](#oracle-invoice-kong) 
* [Summary](#summary)
* [Setup and Pre-requisites](#setup-and-pre-requisites)
* [Deployment](#deployment)
* [Verifying the API Gateway deployment](#verifying-the-api-gateway-deployment)
* [Stop the Kong Gateway](#stop-the-kong-gateway)
---
## Setup and Pre-requisites

1. If not already installed:

- Install Docker on your device (you can use the following link for a guide: [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/))

2. Clone this repository or download the .zip file from GitHub (extract the downloaded zip file)

## Deployment

1. Using a Command Line Interface of your choosing, change directory to the downloaded/cloned repository

2. To deploy the Kong Gateway, run the following command:

    ```
    docker-compose up
    ```

    If you want to deploy the Kong Gateway in detached mode, run the command below:

    ```
    docker-compose up -d
    ``` 

3. A Docker container should now be running with a Kong API Gateway installed

## Verifying the API Gateway deployment

1. On a web browser, go to the Kong Gateway manager<http://localhost:8002>.
2. Click on the `default` workspace.
3. On the left side of the screen, click on `Gateway Services`. From here, you should see a list of 45 services in the Gateway.
4. On the left side of the screen, click on `Routes`. From here, you should see a list of 80 routes in the API Gateway.

## Stop the Kong Gateway

To stop the Kong gateway container, run the following command:
```
docker-compose down
```