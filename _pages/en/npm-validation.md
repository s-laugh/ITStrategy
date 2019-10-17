---
layout: default
title: NPM packages validation for ESDC
ref: npm-validation
lang: en
status: posted
categories: Work In Progress
permalink: /npm-validation.html
---

## NPM packages validation for ESDC

The [NodeJS] is approved software and can be installed on users desktops/laptops.
NPM packages are considered plugins and do not require ARC/EARB endrosement for use.
The following are best practices:

### Verify the Licence

The licence used by the NPM package and all it's dependencies must be open source software (OSS).

> Software licensed under an [Open Source Initiative approved license](https://opensource.org/licenses/alphabetical) or a [Free Software Foundation free software licence](https://www.gnu.org/licenses/license-list.html#SoftwareLicenses) are considered OSS and can be used by the GC.

Using OSS **without modification** does not require that code be shared back.
Using OSS **with modifications** might require that code be shared back if it's under a strong reciprocal licences.
See [GC Guidance on Using OSS - Verify Ownership or Licence](https://github.com/canada-ca/open-source-logiciel-libre/blob/master/en/guides/using-open-source-software.md#verify-open-source-software-ownership-or-licence) for more details on licences.

### Security

NPM packages used and all their dependencies must not have CVEs for the versions being used.

### Tool

{% include npm-validation.html %}
