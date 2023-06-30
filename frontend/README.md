# aws-resume
My resume in AWS

![Diagram](img/image.png)

## Prerequisites

- [GitHub account](https://github.com/join)
- [AWS account](https://aws.amazon.com/free)
- [AWS CLI](https://aws.amazon.com/cli/)
- [AWS Tools for Powershell](https://docs.aws.amazon.com/powershell)
- [Visual Studio Code](https://code.visualstudio.com)
- [Visual Code Extensions](https://code.visualstudio.com/docs/introvideos/extend)
  - [AWS Toolkit for Visual Studio Code](https://aws.amazon.com/visualstudiocode/)
- [AWS IAM User](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-credentials.html)
## Front-end resources

The front-end is a static site with HTML, CSS, and JavaScript. It's static and has a visitor counter. The visitor counter data fetched via an API call to an Lambda Function.

- I am a terrible designer, I used this [template](https://www.styleshout.com/free-templates/ceevee/) to create my site. 
- I'm no JavaScript dev, but this [article](https://www.digitalocean.com/community/tutorials/how-to-use-the-javascript-fetch-api-to-get-data) explains well and in a simple way how to use it to make an API call.
- This is how you can [host website without a web server](https://docs.aws.amazon.com/whitepapers/latest/build-static-websites-aws/use-amazon-s3-website-hosting-to-host-without-a-single-web-server.html)

## Back-end resources

The back-end is an [Event-driven Lamdba Functions](https://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html). When the Function is triggered, it retrieves the DynamoDB item, adds 1 to it, and saves it and returns its value to the caller.

- [Create a DynamoDB Table](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/getting-started-step-1.html)
- [Create a Lambda Function with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
- [Lambda Functions with DynamoDB](https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html)
- You'll have to [enable CORS with Azure Functions locally](https://github.com/Azure/azure-functions-host/issues/1012) and once it's [deployed to Azure](https://docs.microsoft.com/en-us/azure/azure-functions/functions-how-to-use-azure-function-app-settings?tabs=portal#cors) for you website to be able to call it.

## CI/CD Resources

- This is how you can deploy to an S3 Bucket in AWS with [GitHub actions.](https://github.com/jakejarvis/s3-sync-action)