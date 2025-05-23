<h2>How to install the local frontend repository from scratch (on Mac):</h2>

1. You need [NodeJS](https://nodejs.org/en/download) + [yarn](https://yarnpkg.com/getting-started/install):
```
# Download and install Homebrew
curl -o- https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh | bash

# Download and install Node.js:
brew install node@22

# Verify the Node.js version:
node -v # Should print "v22.16.0".

# Download and install Yarn:
corepack enable yarn

# Verify Yarn version:
yarn -v
```
002. You need the [GitHub Personal Access Token](https://github.com/settings/tokens) with the access to: 
* read:packages ✅
* repo ✅
3. Create `.npmrc` file in the root of the project (of the <b>project</b>, not global) and add the following inside:
```
@Cakeiteasy:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:_authToken=ghp_XXXXXXXXXXXXXXXXXXXX
```
❗️ Don't forget to insert your GitHub Token instead of `ghp_...`

004. You need [Angular CLI](https://angular.dev/tools/cli/setup-local): `yarn global add @angular/cli`
5. `yarn install` (sometimes you need `yarn cache clean` before)
6. Follow the current project's README instructions

<b>NOTE:</b> If you have an error `Error: error:0308010C:digital envelope routines::unsupported` during installing packages it means that you have too modern NodeJS version.
To fix it use: `export NODE_OPTIONS=--openssl-legacy-provider` 
