This generates a unified diff email for GitHub's WebHooks in the Settings page of the repositories.
It handles the default Push events only.

This is built using [Serverless](http://serverless.com/) which works ontop of AWS API Gateway and Lambda.

# Requirements #
- AWS Account with privileges to create IAM Roles, Lambda Functions and API Gateway Endpoints
- AWS Profile Configured
- NPM and Node.js

# Getting Started #
1. Install Serverless `npm install serverless -g`
2. Clone the this repository
3. Run `serverless project init` inside the project directory
4. `cd` into the lambda function github-push-notification folder and run `npm install`
5. Modify the github-push-notification/config.json file to match your requirements
6. Deploy using `serverless dash deploy`
7. Log onto the AWS Console and go to API Gateway. Grab the ARN URL for the **github-push-notification** post endpoint and put that into the GitHub Webhook Settings page 

If you modify the template and want to just update the function simply run:
`serverless function deploy`

