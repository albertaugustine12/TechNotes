---
id: GitHub Actions
description: Anuthing Everything about GH actions
slug: githubaction
sidebar_position: 1
tags:
  - GitHub
  - Actions
  - Workflow
---

# GitHub Action

## Tips

**GITHUB_TOKEN**

For newbies of GitHub Actions: Note that the *GITHUB_TOKEN* is NOT a personal access token. A GitHub Actions runner automatically creates a *GITHUB_TOKEN* secret to authenticate in your workflow. So, you can start to deploy immediately without any configuration.

## Workflows
List of workflows referred, used or found something interesting
* [Docusaurus](https://github.com/peaceiris/actions-gh-pages#%EF%B8%8F-docusaurus) 

## Issues

### Setting working directory
We can set a default working directory for a job or we can set it for individual step

**Default working directory for a job**
```yaml
jobs:
  deploy:
    defaults:
      run:
        working-directory: website
```

**For individual step**
```yaml
  deploy:
    name: Deploy to GitHub Pages
    runs-on: ubuntu-latest
    steps:
      - name: Build website
        working-directory: website
        run: yarn build
```

### Failed with exit code 128, Permission Denied
Issue described [here](https://github.com/JamesIves/github-pages-deploy-action/issues/1110)

*Error*
```
Run peaceiris/actions-gh-pages@v3
[INFO] Usage https://github.com/peaceiris/actions-gh-pages#readme
Dump inputs
Setup auth token
Prepare publishing assets
Setup Git config
Create a commit
Push the commit or tag
  /usr/bin/git push origin gh-pages
  remote: Permission to albertaugustine12/TechNotes.git denied to github-actions[bot].
  fatal: unable to access 'https://github.com/albertaugustine12/TechNotes.git/': The requested URL returned error: 403
  Error: Action failed with "The process '/usr/bin/git' failed with exit code 128"
```

Fixed by updating workflow permission for the repo by following this [comment](https://github.com/JamesIves/github-pages-deploy-action/issues/1110#issuecomment-1117481234)



