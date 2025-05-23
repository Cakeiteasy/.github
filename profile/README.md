How to install the local repository from scratch (on Mac):

1. You need [Homebrew](https://brew.sh/)
2. You need NodeJS: `brew install node`
3. You need the [GitHub Personal Access Token](https://github.com/settings/tokens) with the access to: 
	<br>•	read:packages ✅
	<br>•	repo ✅
4. Create `.npmrc` file in the root of the project (of the <b>project</b>, not global) and add the following inside:
  ```
@Cakeiteasy:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:_authToken=ghp_XXXXXXXXXXXXXXXXXXXX
```
<i>Don't forget to insert your GitHub Token instead of `ghp_...`</i>

005. `yarn install` (sometimes you need `yarn cache clean` before)
6. Follow the current project README instructions

NOTE: If you have an error `Error: error:0308010C:digital envelope routines::unsupported` during installing packages it means that you have too modern NodeJS version.
To fix it use: `export NODE_OPTIONS=--openssl-legacy-provider` 
