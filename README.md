
## Dev Environment


```bash
# Dev backend
$ git stash
$ git pull origin dev
$ yarn install
$ yarn migrate:deploy
$ pm2 delete backend-dev
$ pm2 start "yarn start" --name "backend-dev"  --time
```




```bash
# Dev Admin
$ git stash
$ git pull origin dev
$ yarn install
$ pm2 delete admin-dev
$ pm2 start "yarn start" --name "admin-dev"  --time
```


```bash
# Dev WebSite
$ git stash
$ git pull origin dev
$ yarn install
$ pm2 delete Website-Dev
$ pm2 start "yarn start" --name "Website-Dev"  --time
```


## Staging Environment

```bash
# Stage Backend
$ git stash
$ git pull origin staging
$ yarn install
$ yarn migrate:deploy
$ yarn build
$ pm2 start "yarn start:prod" --name "backend-staging"  --time
```

```bash
# Stage Admin
$ git stash
$ git pull origin staging
$ yarn install
$ yarn build
```

```bash
# Stage Website
$ git stash
$ git pull origin staging
$ yarn install
$ yarn build
$ pm2 start "yarn start" --name "Website-Staging"  --time
```

