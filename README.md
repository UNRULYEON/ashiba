# ashiba

React components for building applications

## Installation

Install the package with `npm i ashiba` or `yarn add ashiba`

## Publishing to NPM

Before you publish the package, make sure you're logged in with `yarn login`. You only have to do this once.

1. Update the version in `package.json` following [semver](https://semver.org/) ([Cheatsheet](https://devhints.io/semver)). Do this in the `develop` branch.
2. It speaks for itself that the `develop` branch has to be tested and confirmed that the package works as expected.
3. Push only the version bump in the `package.json` to the **remote** `develop` branch with as descripton:

```md
Bumped version to vX.X.X
```

The `X.X.X` should correspond with the version in the `package.json`.

At this point, you can make a [pull request](https://github.com/UNRULYEON/ashiba/compare) on **Github** from `develop` → `master`.

1. Pull the changes on the master branch on you local machine.
2. Create a tag **on the `master` branch** with the same version as in the `package.json` with: `git tag -a <VERSION>`
3. The message should be a short description of what's included since the last tag:

```md
Added:
• x

Fixed:
• x
```

4. Build the project with `yarn build`
5. Pushed the tag to Gitlab with: `git push --tags`
6. Publish the package with: `yarn publish --access public`. Hit enter when yarn asks: `question New version:`
