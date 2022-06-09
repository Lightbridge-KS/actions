# Push files to Repo or Branch

## Push to Branch

To push file to orphan branch named `output` in the same repo

### 1. Create Orphan Branch

Adapted from [this tutorial](https://shannoncrabill.com/blog/git-orphan-branches/)

Create new `output` orphan branch with no commit history by:

```shell
git checkout --orphan output
```

Remove all files in this new branch with:

```shell
git rm -rf .
```

Create README, commit, and push

```shell
echo "Output" > README.md
git add .
git commit -m "Create orphan branch with README"
git push -u origin output
```

Go back to main

```shell
git switch main
```

### 2. Create GitHub Actions

```r
usethis::use_github_action(url = "https://github.com/Lightbridge-KS/lb-actions/blob/main/push-files/push-files.yml")
```

-   Modify the YAML file it according to your need

-   Add repository secrets `COPY_FILES_ACROSS_REPO`. (Repo Setting -> Secrets -> New repository secrets)