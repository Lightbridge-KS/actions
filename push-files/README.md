# Push files to Repo or Branch

## Push to Branch

To push file to orphan branch in the same repo

### Create Orphan Branch

[tutorial](https://shannoncrabill.com/blog/git-orphan-branches/)

```shell
git checkout --orphan output
```

this will create new `output` orphan branch with no commit history

```shell
git rm -rf .
```

Will remove all files in this new branch

### Create GitHub Actions

```r
usethis::use_github_action(url = "URL-of-the-YAML")
```

