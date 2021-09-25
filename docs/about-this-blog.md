---
order: 1
title: About This Blog
---

Here we've built a blog that is able to:

- Generate posts from markdown files
- Generate static syntax highlighting
- Deploy to a cloud platform

## Generate Posts from Markdown Files

We use a `ng-zorro-antd` Node.js script to generate compiled Angulat modules from a set of markdown files. Each post represents a compiled JavaScrip file loades via lazy-loading.

## Generate Static Syntax Highlighting

To generate static syntax highlighting (which is static HTML), we use `prismjs` on Node.js. This way we do not need to include `prismjs` JavaScript in our web application.

## Deploy to a Cloud Platform

We use Red Hat [OpenShift Online](https://www.openshift.com/products/online/) public cloud
with [Source-to-Image](https://docs.openshift.com/container-platform/3.11/architecture/core_concepts/builds_and_image_streams.html#source-build) (S2I) build
and [Recreate Strategy](https://docs.openshift.com/container-platform/3.11/dev_guide/deployments/deployment_strategies.html#recreate-strategy) with downtime from 5 to 20 seconds.
More resources are needed in order to use [Advanced Deployment Strategies](https://docs.openshift.com/container-platform/3.11/dev_guide/deployments/advanced_deployment_strategies.html)
and fully authomatic deployments.
