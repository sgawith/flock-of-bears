# Creating a new Lambda function
To create a new function, use the following syntax.

For a Java function:

`aws lambda create-function --function-name <function name> --runtime java8 --role <full user role name, including arn: prefix> --handler <package>.<class>::<method> --zip-file fileb://<path to JAR file>`

If your function has already been created, but you want to update the code, use [[Updating a Lambda function]] instead.

#aws #lambda