# hello-api

This is a standard vanilla type AWS SAM project deploying API Gateway with Lambda. 

It is demonstrating how to use Route53 zone (configured in http://github.com/OperationalFallacy/CrossRouter53 repository) for creating custom domains names for API and with ACM certificates.

## Deploy the sample application


```bash
sam build && sam deploy --stack-name hello-api --profile dev
```

You can find your API Gateway Endpoint URL in the output values displayed after deployment: `https://hi-api.dev.naumenko.ca/Prod/hello/`


## Cleanup

To delete the sample application that you created, use the AWS CLI. Assuming you used your project name for the stack name, you can run the following:

```bash
aws cloudformation delete-stack --stack-name hello-api
```
