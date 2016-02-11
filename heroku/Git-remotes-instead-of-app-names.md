### Use git remotes to manage apps for multiple environments

#### Setup

```
heroku git:remote -r qa -a mycoolapp-com-qa`
heroku git:remote -r prod -a mycoolapp-com-production
```

#### Usage

Instead of running this:

`heroku config:get DATABASE_URL -a website-com-production`

Run this:

`heroku config:get DATABASE_URL -r prod`

#### Benefits

- Less typing
- You don't have to remember all your Heroku app names
- Protection against accidentally running commands in the wrong app/environment.
  - The Heroku CLI will default to the git remote named `heroku` if one exists. This is often undesirable if you have multiple Heroku apps for a repo.
