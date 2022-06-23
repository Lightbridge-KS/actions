# Quarto Publish

-   [`quarto-publish-netlify.yaml`](quarto-publish-netlify.yaml)

## Publish to Netlify

Adapted from [this example](https://github.com/quarto-dev/quarto-actions/blob/main/examples/example-01-basics.md)

To use GHA

```r
usethis::use_github_action(url = "URL-of-the-YAML")
```

For first publication to Netlify, run:

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

