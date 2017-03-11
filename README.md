# Prtocf - Pull Request to Cloud Foundry

Prtocf will simplify checking of PRs (Pull Requests) by deploying the branch to cloud foundry. 
For now it is only intended for use with jekyll sites that are built with CircleCI.

Inspired by [QA Fire](https://github.com/AusDTO/qa-fire)

## How it works

When a PR is created:
1. Circle will build the branch.
2. If the tests pass, Circle sends a webhook to Prtocf.
3. Prtocf will fetch the Circle build artifacts, and push them to Cloud Foundry.

When the PR is closed:
1. Github sends a webhook to Prtocf.
2. Prtocf will delete the Cloud Foundry application.
