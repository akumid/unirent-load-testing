# unirent-load-testing

Load test is scheduled to run daily at midnight UTC and on push to main branch.
Running on AWS Lambda using Github Actions not working. Not sure why OIDC connection is failing

## Running locally

Install Artillery

```sh
npm install -g artillery@latest
```

Create .env.local file and put API Key value

Then run test locally

```sh
artillery run artillery/simple.yml --dotenv .env.local
```

## Running on cloud

https://www.artillery.io/blog/github-action-fargate-lambda
https://www.artillery.io/docs/load-testing-at-scale/aws-lambda
https://github.com/aws-actions/configure-aws-credentials#configure-aws-credentials-for-github-actions
