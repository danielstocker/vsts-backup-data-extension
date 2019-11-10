# Backup Data Extension
This extension contains a variety of pipeline tasks that help you extract data from Azure Repos (or other source control services) during a pipeline execution.

## Tasks currently available

- Pull Git Repo
  - pulls any git repo during build into a folder or into the working directory
- Commit to Git
  - pushes a sub folder or everything in the working directory into a specified git repo
- Export Release Definitions
  - exports all (or a subset of all) release definitions from a specified Azure DevOps organisation
  - definitions can be downloaded into a sub folder or the current working directory

#### All tasks are pipeline tasks
#### All tasks work on Windows-based agents only

## Use cases

- Use the git pull task to get everything in a Git repo, then use Git push to create a copy of this repo in a different location. 

- Download one or more release definitons whenever a pipeline is executed
- These can then be pushed to a differen Azure DevOps org or an Azure DevOps server deployment

## Code

Available on GitHub

## Parameters and Settings


#### Pull Git Repo

- Source Repo URI
- Username 
  - if required
- Password 
  - if required (also supports PAT)
- Source Branch 
- Drop dir

#### Commit to Git

- Destination Repo URI
- Username 
  - if required
- Password 
  - if required (also supports PAT)
- Destination Branch
- Git user name and e-mail 
- Commit Message 
- Target path

#### Export Release Definitions

- API endpoint URI
- Username 
  - if targeting TFS 2015
- Password or PAT 
  - if targeting TFS 2017 or newer and/or Azure DevOps 
- Filter
  - simple "Contains" filter to narrow the amount of definitions downloaded
- Drop dir
