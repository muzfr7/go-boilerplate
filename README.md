# Go Boilerplate

## Overview
The basic starter boilerplate to follow when building Go apps. It is inspired by Standard Go Project Layout and Clean Architecture by Uncle Bob.

## Directories

### /cmd
Main entrypoints for each app in this project. The directory name for each app should match the name of the executable you want to have eg: `/cmd/myapp`

> Don't put a lot of code in the application directory. It's common to have a small main function that imports and invokes the code from the /internal and /pkg directories and nothing else.

### /internal
Private application and library code, which you don't want others importing in their applications or libraries.

If the code is not reusable or if you don't want others to reuse it, put it in this directory.

> This layout pattern is enforced by the Go compiler itself. You are not limited to the top level internal directory. You can have more than one internal directory at any level of your project tree. 

> This directory is a better way to ensure your private packages are not importable because it's enforced by Go.

### /pkg
Library code that's ok to use by external applications eg: `/pkg/mypubliclib`. Other projects will import these libraries expecting them to work, so think twice before you put something here.

If you think the code can be imported and used in other projects, then it should live in the `/pkg` directory.

This directory is a good way to explicitly communicate that the code in this directory is safe for use by others.

### /resources

### /config
Configuration file templates or default configs, possibly to be mapped from .env files.

### /bin
### /deploy
### /docs
### /testdata



