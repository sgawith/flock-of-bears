# Connecting a local clone to an existing heroku app
To connect a git clone to an existing Heroku application (rather than creating a new one):

`git remote add heroku git@heroku.com:<project name>.git`
`heroku git:remote -a <project-name>`

Source: [stackoverflow.com](https://stackoverflow.com/questions/5129598/how-to-link-a-folder-with-an-existing-heroku-app)

#heroku #git