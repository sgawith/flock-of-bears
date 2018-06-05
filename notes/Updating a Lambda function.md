# Updating a Lambda function
To update an existing function with a new JAR source:

`aws lambda update-function-code --function-name <function name> --zip-file fileb://<JAR file>`

If the function has not previously been defined, you'll need to create a new one instead: [[Creating a new Lambda function]] 

#aws #lambda