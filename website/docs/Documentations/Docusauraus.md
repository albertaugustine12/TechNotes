---
id: Docusaurus
description: Documenting steps implemented for a docusaurus project as a guide
slug: /docusaurus
sidebar_position: 2
tags: 
  - Docusaurus
  - Documentation
---

# Docusaurus

Official doc - [docusaurus.io](https://docusaurus.io/)

## Example Project

This documentation project. Followed steps in **Getting started** to set up the project. 

### Current project setup {#my-docusaurus-project-setup}


- Create project and run it
```bash
npm init docusaurus@latest my-website classic

OR 

npx create-docusaurus@latest my-website classic --typescript

cd my-website
npm run start
```
 - Only *doc* site. *Blog* disabled
```js
  blog: false, // Optional: disable the blog plugin
```
- Removed intro page. Updated homepage to be the starting doc page
```js
  docs: {
        routeBasePath: '/', // Serve the docs at the site's root
    }
```

### Gihhub pages setup
Followed instructions in the [documentation](https://docusaurus.io/docs/deployment#deploying-to-github-pages) to use workflow to build and publish the doc site.

GH Pages workflow reference - https://github.com/peaceiris/actions-gh-pages#%EF%B8%8F-docusaurus





