## Installation

```sh
git clone git@github.com:springload/react-d3-integration.git
cd react-d3-integration
nvm install
npm install
```

## Working on the project

> Everything mentioned in the installation process should already be done.

```sh
# Use the right node version
nvm use
# Start the server and the development tools.
npm run start
# Builds frontend assets for production.
npm run build
# Runs tests.
npm run test
```

## Deploying the project

```sh
# First make sure your master is up to date.
cd react-d3-integration
git fetch --all
git checkout master
git pull
git push origin master
# Then build the project
npm run build
# Follow the instructions in the build command
git commit -am "Save local changes"
git checkout -B gh-pages
git add -f build
git commit -am "Rebuild website"
git filter-branch -f --prune-empty --subdirectory-filter build
git push -f origin gh-pages
git checkout -
```
