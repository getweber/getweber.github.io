---
layout: post
title: Big Changes - Systemd and More
---

Today marks the end of a long development effort to modernize Weber's deployment, as well as many code cleanups. The results were pushed to the master branches, while the previous code was published under a new maintenance branch - `maint-1.0`.

## Systemd Deployment

The biggest change without a doubt is the move to systemd as a primary deployment method. This had many reasons, like subtle bugs in `supervisor` and reliability issues, but the biggest reason is that we simply believe systemd is just better.

Weber now supports deployment to Debian (8.1 and later), Ubuntu (15.04 and later), CentOS (7.0 and later) and Arch Linux out of the box.

## Python 3.4 by Default

Unlike 3rd party libraries you ship without knowing what version the eventual user would use, Weber is different. We believe it makes little sense to cling to Python 2.x for webapps, when there are so many benefits of moving to 3.x.

We switched the default deployment to 3.4, and of course if you prefer 2.x you can change the deployed version yourself after cloning.

## Name Changes

It has become apparent to us that most real uses of Weber would need frontend code at some point, and that is when it makes sense to embrace some convention of layout out the project. This is why we believe the full version of Weber (formerly `weber-frontend`) should be the default for new projects. This is why we renamed it to simply `weber`, and also changed `weber-minimal` to `weber-micro`.

That's it for now - keep hacking away, and feel free to leave feedback and open issues whenever necessary.
