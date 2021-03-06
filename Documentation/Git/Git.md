---
layout: default
title: Git
nav_order: 20
permalink: /documentation/git
---

# Git
We use Git as version control system.

## Git Repository naming
We do not use spaces in Git Repository names. Instead we use dashes to separate words and Pascal Casing is allowed within words.
e.g.:
- HsM-Software-Development-Standards
- HsM-CatalogService
- HsM-DigitalTwinService

## Dividing Repositories

### One repository per release product
If two software products will at some point have different release cycles they go into different repositories. I.e. code that is published together under a single version number goes into the same repository. Code that has parts with different version numbers has to be split into separate repositories. 

### Separate repositories for files which might be needed by multiple projects
This promotes sharing and code reuse, and is highly recommended. This also implies an isolated release cycle.

### Read access control is at the repo level
If someone has access to a repository, they have access to the entire repo, all branches, all history, everything. If you need to compartmentalize read access, separate the compartments into different repositories. For Hagleitner this is especially important since we work with many partners.

## Commiting to a Repository
Commit early and commit often. Write useful commit messages. First line shall be a short (<= 50 character) summary of the change. More details can follow.

## Repository Maintenacne
* Delete merged branches
* Delete stale branches
* Empty your stash

## Workflow
### Gitflow
We use the GitFlow Workflow for most of our projects (https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

#### Branch names (mind capitalization):
* develop
* master
* feature \<Jira-issue-number\>_\<issue-name-with-dashes\>
* release/\<releasename>: 
* bug-fix/\<Jira-issue-number>_<issue-name-with-dashes>
* hotfix/v\<2.1.2\> (semantic version)

#### Releases and hotfixes
* Release Branches are branched from develop, version push happens on release branch
* Once release work is finished be merge to master and we tag the release
* We create a hotfix branches from master whenever we need hotfixes on an existing release (we branch from the release-tagged commit)

#### Feature-branching
* We may use Feature Branch Workflow for smaller projects (https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
  
Branch names (mind capitalization)
* master
* feature/<Jira-issue-number>_<issue-name-with-dashes>
* bug-fix/<Jira-issue-number>_<issue-name-with-dashes>

Tagging:
* We create tags on master branch commits for every release