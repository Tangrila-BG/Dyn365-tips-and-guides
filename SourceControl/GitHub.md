# Dynamics 365 source control in GitHub

## Setting up a repo

Firstly, I'd like to point out that trying to do this with symbolic links is not worth the trouble and in the end you're more likely to fail than succeed. I wasted 2 days trying to make it work and in the end I went with the simpler option described below.

* Create your repository using the github website, leave it empty. - optional
* Go to the AOSService folder(the root of the PackagesLocalDirectory)
* Optionally create a Projects folder where your solutions and projects will live
* Open your favorite terminal in elevated.
* Type "git init"
* Type "git remote add origin (url to your repo)"
* Type "git fetch"
* Type "git checkout master(or an already created branch"
* Copy-Paste and repurpose the text below on the first line of the gitignore file

~~~text
### My Dynamcis 365 custom ignore/includes ###

# Ignore root
/*

# Include
!.gitignore
!.gitattributes

# Include projects
!Projects

# Include model folder
!PackagesLocalDirectory

# Exclude all models
PackagesLocalDirectory/*

# Include all my prefixed models
!PackagesLocalDirectory/MyPrefix*/

# Exclude all my prefixed models sub-directories
PackagesLocalDirectory/MyPrefix*/*

# Include MyPrefixAnalytics model objects and descriptor
!PackagesLocalDirectory/MyPrefixAnalytics/MyPrefixAnalytics
!PackagesLocalDirectory/MyPrefixAnalytics/Descriptor

# Include MyPrefixSales model objects and descriptor
!PackagesLocalDirectory/MyPrefixSales/MyPrefixSales
!PackagesLocalDirectory/MyPrefixSales/Descriptor

# Include MyPrefixCore model objects and descriptor
!PackagesLocalDirectory/MyPrefixCore/MyPrefixCore
!PackagesLocalDirectory/MyPrefixCore/Descriptor

#/# My Dynamcis 365 custom ignore/includes #/#
~~~

Now you can get the status, commit, push and pull

## Complex Repo with submodules

Using the [Setting up a repo](#setting-up-a-repo) you can create multiple repos, then create a new repo that has a complex folder structure that in it has references to the other created repos