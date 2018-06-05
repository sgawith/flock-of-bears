# Running a Serverless function
To run a function locally:

`sls invoke local -f <function name>`

You can also provide a sample event in JSON format:

`sls invoke local -f <function name> -p <json file path>`

When running locally, both the function output and any console log events will be shown.

You can also run the published version of the function:

`sls invoke -f <function name>`

When running remotely, you only see the output, not the logs. Remote logs can be viewed in other ways - see note [[Viewing Lambda function logs]]

#aws #aws-lambda #serverless