# Quarto Publish

-   [`quarto-publish-netlify.yaml`](quarto-publish-netlify.yaml)

## Publish to Netlify

Adapted from [this example](https://github.com/quarto-dev/quarto-actions/blob/main/examples/example-01-basics.md)

Use GHA

```r
usethis::use_github_action(url = "https://github.com/Lightbridge-KS/actions/blob/main/quarto-publish/quarto-publish-netlify.yaml")
```

For first publication to Netlify, login to desired Netlify account, run:

```sh
quarto publish netlify
```

This will add `_publish.yml` to the repository

```yaml
- source: project
  netlify:
    - id: <netlify-site-id-string>
      url: 'https://your-site.netlify.app'
```

Add GitHub Repository Secrets:

 - `NETLIFY_AUTH_TOKEN`: [Personal access tokens](https://app.netlify.com/user/applications#personal-access-tokens) > New access token


Push to GitHub!