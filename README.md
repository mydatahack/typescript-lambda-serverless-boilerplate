# typescript-lambda-launch-darkly-get-flags

AWS Lambda function boilerplate with TypeScript. It will give you a head start on building AWS lambda with TypeScript. Please make sure to add the custom_config with your AWS account information as in step 2 of the Setup section.

The example function simply retrieves data from an API endpoint and return it from API gateway.

serverless-webpack plugin enables transiplation through webpack before deployment. Once webpack & tsconfig are set, everything works like JavaScript (see the [JavaScript lambda boilerplate](https://github.com/mydatahack/nodejs-lambda-serverless-boilerplate)).

### Setup

(1) Install all modules
```bash
npm i
```

(2) Create custom_config folder in the root and add account.yml.

The yaml file contains your aws environment information including Account Id, region and deployment bucket.

```yaml
ACCOUNT_ID: "your account id"
REGION: "your aws region"
DEPLOYMENT_BUCKET: "s3 deployment bucket name"
```

### Running Test

It uses mocha for unit & integration tests. Istanbul for coverage.

```bash
# unit test
npm test
# integration test
npm run integration
```

### Deployment

```bash
sls deploy --stage dev1
```

### Checking endpoint

```bash
curl -H "x-api-key: <api key" -X GET https://url
```

### Reference

Tools

- [serverless](https://serverless.com/)
- [webpack](https://webpack.js.org/)
- [serverless-webpack](https://github.com/serverless-heaven/serverless-webpack)
- [source-map-support](https://www.npmjs.com/package/source-map-support)

Configuration & Miscellaneous Reference

- [serverless variables](https://serverless.com/framework/docs/providers/aws/guide/variables/)
- [AWS API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html)
- [JavaScript's strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
- [Setting up tslint auto save](https://www.mydatahack.com/how-to-auto-fix-lint-on-save-with-vs-code-tslint-extension/)
- [TypeScript compiler options](http://www.typescriptlang.org/docs/handbook/compiler-options.html)
- [Nodejs AWS Lambda Boilerplate](https://github.com/mydatahack/nodejs-lambda-serverless-boilerplate)
- [Istanbul with Moca & TypeScript](https://istanbul.js.org/docs/tutorials/typescript/)