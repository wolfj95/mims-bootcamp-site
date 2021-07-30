# MIMS Bootcamp Course Page
This repository hosts the content for the MIMS Bootcamp in a statically generated Hugo site.

## Install
1. Clone the `mims-bootcamp-site` repository with it's submodules:

        git clone --recurse-submodules https://github.com/wolfj95/mims-bootcamp-site.git

1. Install hugo:

        brew install hugo

## Develop
To develop, start by cloning the repo, installing Hugo (the static site builder we're using for this project), and running a server to host a local version of the site:

    cd mims-bootcamp-site
    hugo server
    open http://localhost:1313

All additions to the website should be developed on a feature branch before they are merged to the master branch (anything in the master branch will be live on the website!). To make a new branch:

    git checkout -b branch-name

The Hugo will automatically build the local version as you make changes in the branch. 

Don't forget to add/commit/save your work as you go:

    git add file_you_changed
    git commit
    git push

## Deploy
Once you're ready to deploy a change to the website, run the `hugo` command without any parameters.
The site will build in a directory called `python-bootcamp`. Upload this directory to your web server
and you're ready to roll!
