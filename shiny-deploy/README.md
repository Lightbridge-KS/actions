# Deploy Shiny App

Inspired from [Shiny App Deployment GHA](https://github.com/r-lib/actions/tree/v2-branch/examples#shiny-app-deployment)

`{renv}` is required

## Set Repo Secrets

Set 3 `rsconnect` repository secrets:

-   `RSCONNECT_USER`
-   `RSCONNECT_TOKEN`
-   `RSCONNECT_SECRET`

Obtain the token and secret for configuring `rsconnect`: [see here](https://shiny.rstudio.com/articles/shinyapps.html)

## Add `.rscignore`

Add `.rscignore` to list files that will not be deployed.

```r
usethis::use_github_file(path = "https://github.com/Lightbridge-KS/actions/blob/main/shiny-deploy/.rscignore")
```

## GHA

```r
usethis::use_github_action(url = "https://github.com/Lightbridge-KS/actions/blob/main/shiny-deploy/shiny-deploy.yaml")
```

-   Config `ACCOUNT` and `APPNAME` in the yaml

Git Push !!