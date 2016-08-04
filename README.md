# lerna-dependency-issue-demo
Showcasing an issue where a dependency of dependency is not being installed in main project's node_modules, causing a broken build

This sowcases a bug I'm also activley trying to resolve, see the issue here: https://github.com/lerna/lerna/issues/297


I noticed that `lerna bootstrap` does not install dependencies are not installed into node_modules.

Let's say I have two projects in my repo:
```
repo
|_ main-project
|_direct-dependency
```

direct-dependency had `lodash` as a dependency.

running `lerna bootstrap` will not install lodash in `main-project/node_modules`
