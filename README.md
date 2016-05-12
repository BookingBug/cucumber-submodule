# Cucumber Boilerplate git submodule

This repository is a copy of the cucumber boilerplate `tests` directory.

The reason to chain these repos together is so we can develop the main repo https://github.com/maxmckenzie/cucumber-boilerplate with linting, babel etc and then pull in only the `tests` directory for separate projects.

This means that we can maintain updates across multiple projects whilst allowing cucumber-seed to take its own direction. Brain space is being used to figure out how to fork it into a npm package as a more developed test suite. BUt for the moment this way seems to work nicely as a stop gap.

# Including the repo in another git repo.

To implement this and maintain updates its suggested you include this repo as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules). To do this follow the steps below.

1. clone

Clone this repo as a submodule into an existing project with the folder name `test`

`git submodule add https://github.com/maxmckenzie/cucumber-submodule.git test`

it will create the folder test at the root of your project

## Backporting changes to this repo
If you've fixed an error added a change you want to port back to this repo as long as your in the root of the test directory any commits 

## Commiting to your own project
Just commit from the root of your project as you would do normally and it'll commit the custom code you've added to the test directory without affecting this repo.

## Get updates to the submodule
just run `git submodule update`
