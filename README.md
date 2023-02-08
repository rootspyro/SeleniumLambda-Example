# SeleniumLambda-Example
just an example of selenium deployment in lambda with docker 

## Technologies :computer:
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

## Deployment :fire:

### 1. Clone the repository
```shell
git clone https://github.com/rootspyro/SeleniumLambda-Example.git
cd SeleniumLambda-Example
```

### 2. Deploy the app to lambda
This step requires the serverless framework, which will be the deployment with our configuration in serverless.yml and Dockerfile.

If you do not have serverless already installed you can install it with Nodejs. Run the command `npm i -g serverless`.

You will find the documentation on how to configure aws credentials here:: [AWS - Config Credentials](https://www.serverless.com/framework/docs/providers/aws/cli-reference/config-credentials).

__For deploy the function run the command:__
```shell
sls deploy
```
Serverless framework will do the following:
- Create a .serverless folder in the local project
- Build the Docker image
- Deploy the docker image to AWS ECR
- Create a S3 bucket
- Upload the .serverless folder to the s3 bucket
- Create a Lambda function with the Docker image created


And that's it, deployment complete! :confetti_ball:
