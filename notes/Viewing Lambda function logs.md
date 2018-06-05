# Viewing Lambda function logs
Logs for Lambda functions executed on the server, whether created through Serverless or not, is possible through Cloudwatch. From the left menu, just select Logs, and you should see a log group for your function.

If a function has been deployed through Serverless, you can also view the logs through the terminal:

`sls logs -f hello`

#aws #aws-lambda #serverless