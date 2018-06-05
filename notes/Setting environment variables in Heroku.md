# Setting environment variables in Heroku
To view and amend the environment variables in your remote Heroku instance, use the following commands:

Set a variable:
`heroku config:set GITHUB_USERNAME=joesmith`

Print all the current variables:
`heroku config`

Print a specified variable:
`heroku config:get GITHUB_USERNAME`

Remove a variable:
`heroku config:unset GITHUB_USERNAME`

Source: [heroku.com](https://devcenter.heroku.com/articles/config-vars)

#heroku #environment_variables