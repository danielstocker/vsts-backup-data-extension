# vsts-backup-data-extension
A collection of Azure Pipeline tasks that allow you to backup data from Azure Repos/Pipelines at the time of a pipeline execution. 
(for example: download a Git repo and commit its content to another repo, download latest version of release definitions, etc.)

### Parameters and Settings

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
