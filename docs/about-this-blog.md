---
order: 1
title: About This Blog
---

Here we've built a blog that is able to:

1. Generate posts from markdown files
2. Generate static syntax highlighting
3. Deploy to a cloud platform
4. Simulate static content

## Generate Posts from Markdown Files

We use a `ng-zorro-antd` Node.js script to generate compiled Angular modules from [a set of markdown files](https://github.com/cioina/alexei-cioina.b9ad.pro-us-east-1.openshiftapps.com/tree/main/posts).
Each post represents a compiled JavaScrip file that loads via lazy-loading.

## Generate Static Syntax Highlighting

To generate static syntax highlighting (which is static HTML,) we use `prismjs` on Node.js. This way, we do not need to include `prismjs` JavaScript in our web application.

## Deploy to a Cloud Platform

We use Red Hat [OpenShift Online](https://www.openshift.com/products/online/) public cloud
with [Source-to-Image](https://docs.openshift.com/container-platform/3.11/architecture/core_concepts/builds_and_image_streams.html#source-build) (S2I) build
and [Recreate Strategy](https://docs.openshift.com/container-platform/3.11/dev_guide/deployments/deployment_strategies.html#recreate-strategy) with short downtime.
More resources are needed in order to use [Advanced Deployment Strategies](https://docs.openshift.com/container-platform/3.11/dev_guide/deployments/advanced_deployment_strategies.html)
and fully automatic deployments.

## Simulate Static Content

We've found [a GitHub repository](https://github.com/dwightwatson/dwightwatson.com) that satisfies all 4 conditions. Well, in fact, it generates a static website, so condition 4 is not
just simulated. In contrast, [this GitHub repository](https://github.com/dwightwatson/neontsunami-laravel) uses Laravel's Blade template and a MySQL database to
[generate posts](https://github.com/dwightwatson/neontsunami-laravel/blob/master/resources/views/posts/show.blade.php) on the server-side. It means that every time you access a post,
your web browser makes a request to the server and the server will get the content from the database and render HTML (BTW, [here](https://github.com/cioina/neontsunami) is a version adapted for OpenShift.) Even if Blade caches the result, every request creates a connection to the database (We do not consider [Laravel Octane](https://laravel.com/docs/8.x/octane) here.) Static websites do not need a database and the content is cached on the user's side. So, the user makes less requests to the server.

How do we simulate static content? All the posts from this blog are Angular compiled JavaScript files that are cached on the user's side.

## Compare Different Tools for Static Content Generation

[Here](https://docs.astro.build/comparing-astro-vs-other-tools/) is a compact comparison between [Astro](https://github.com/snowpackjs/astro) and different tools for static content generation.
