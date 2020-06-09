---
title: Infrastructure - Principle of Least Privilege
published: false
description: Recommendations of what a Service should and should not do in regards to infrastructure and Principle of Least Privilege.
tags: architecture, microservices, security, scale
//cover_image: https://direct_url_to_image.jpg
---

## Infrastructure - A Service Cannot

* Create mutable or shared resources.
* Drop mutable or shared resources.
* Alter mutable or shared resources.

## Infrastructure - A Service must

On Start up:

* Have all resource requirements defined
* Verify all required resources are accessible.
* If possible, verify RBAC roles are configured.
* Alert and fail if resources are not available or accessible.

## Data - A Service must

Release / Updates

* Perform any Data Updates (Migrations) outside of the application logic
* Create compatible or versioned migrations.
* On Startup, verify the the schema version is compatible
