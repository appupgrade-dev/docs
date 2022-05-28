## App Upgrade CLI

### Official Command Line Interface

* [Installation](#installation)
* [Usage](#usage)
* [Commands](#commands)

# Installation
Install via NPM
```sh-session
$ npm install -g appupgrade-cli
```

Install via Docker image
```sh-session
$ docker pull appupgrade/appupgrade-cli
```

```sh-session
Running the image:

$ docker run appupgrade/appupgrade-cli --help
$ docker run appupgrade/appupgrade-cli <COMMAND> <SUBCOMMAND> <ARGS>
```

# Usage
```sh-session
$ appupgrade-cli --version
appupgrade-cli/0.0.0 win32-x64 node-v16.0.0

$ appupgrade-cli --help
CLI tool for App Upgrade.

VERSION
  appupgrade-cli/0.0.0 win32-x64 node-v16.0.0

USAGE
  $ appupgrade-cli [COMMAND]

TOPICS
  auth     Authenticate with App Upgrade!
  plugins  List installed plugins.
  project  Manage project!
  user     User details!
  version  Manage version!

COMMANDS
  commands  list all the commands
  hello     Hello from App Upgrade!
  help      Display help for appupgrade-cli.
  plugins   List installed plugins.
  update    update the appupgrade-cli CLI

$ appupgrade-cli --help <TOPIC>
Ex: appupgrade-cli --help auth

$ appupgrade-cli --help <COMMAND>
Ex: appupgrade-cli --help hello

$ appupgrade-cli --help <TOPIC> <COMMAND>
Ex: appupgrade-cli --help auth login
```

# Commands
* [`appupgrade-cli hello`](#appupgrade-cli-hello)
* [`appupgrade-cli auth login`](#appupgrade-cli-auth-login)
* [`appupgrade-cli auth logout`](#appupgrade-cli-auth-logout)
* [`appupgrade-cli user me`](#appupgrade-cli-user-me)
* [`appupgrade-cli project create`](#appupgrade-cli-project-create)
* [`appupgrade-cli project update`](#appupgrade-cli-project-update)
* [`appupgrade-cli project list`](#appupgrade-cli-project-list)
* [`appupgrade-cli project get`](#appupgrade-cli-project-get)
* [`appupgrade-cli project delete`](#appupgrade-cli-project-delete)
* [`appupgrade-cli project change-api-key`](#appupgrade-cli-project-change-api-key)
* [`appupgrade-cli version create`](#appupgrade-cli-version-create)
* [`appupgrade-cli version update`](#appupgrade-cli-version-update)
* [`appupgrade-cli version list`](#appupgrade-cli-version-list)
* [`appupgrade-cli version get`](#appupgrade-cli-version-get)
* [`appupgrade-cli version delete`](#appupgrade-cli-version-delete)
* [`appupgrade-cli version check-version`](#appupgrade-cli-check-version)

## `appupgrade-cli-hello`
```sh-session
appupgrade-cli hello
Hello from App Upgrade! (./src/commands/hello/hello.ts)
```
## `appupgrade-cli-auth-login`
```sh-session
appupgrade-cli auth login --email=<EMAIL> --password=<PASSWORD>
```
## `appupgrade-cli-auth-logout`
```sh-session
appupgrade-cli auth logout
```
## `appupgrade-cli-user-me`
```sh-session
appupgrade-cli user me
```
## `appupgrade-cli-project-create`
```sh-session
appupgrade-cli project create  --name=Wallpaper --description="created using cli”
```
## `appupgrade-cli-project-update`
```sh-session
appupgrade-cli project update  --name=Wallpaper --description="updated using cli”
```
## `appupgrade-cli-project-list`
```sh-session
appupgrade-cli project list
```
## `appupgrade-cli-project-get`
```sh-session
appupgrade-cli project get —projectId=6252140e6f35ca0027f1900c
```
## `appupgrade-cli-project-delete`
```sh-session
appupgrade-cli project delete --projectId=62916711766f9c00273a61ae
```
## `appupgrade-cli-project-change-api-key`
```sh-session
appupgrade-cli project change-api-key --projectId=629167fe766f9c00273a61c7 --xApiKey=<YOUR_CURRENT_API_KEY>
```
## `appupgrade-cli-version-create`
```sh-session
appupgrade-cli version create --projectId=6252140e6f35ca0027f1900c --appName=”Wallpaper app” --appVersion=1.0.1 --platform=android --environment=production --forceUpgrade=true --message="please update”
```
## `appupgrade-cli-version-update`
```sh-session
appupgrade-cli version update --projectId=6252140e6f35ca0027f1900c --versionId=627ca8af732bcecab45351cc --appName=”Wallpaper app” --appVersion=1.0.1 --platform=android --environment=production --forceUpgrade=true --message="please update”
```
## `appupgrade-cli-version-list`
```sh-session
appupgrade-cli version list --projectId=6252140e6f35ca0027f1900c
```
## `appupgrade-cli-version-get`
```sh-session
appupgrade-cli version get --projectId=6252140e6f35ca0027f1900c --versionId=627ca8af732bcecab45351cc
```
## `appupgrade-cli-version-delete`
```sh-session
appupgrade-cli version get --projectId=6252140e6f35ca0027f1900c --versionId=627ca8af732bcecab45351cc
```
## `appupgrade-cli-check-version`
```sh-session
appupgrade-cli version check-version --xApiKey=ODdiNzg4NmQtNTZiMS00ZTFmLTk0YWMtOGRjYjM3M2UwYjE2 --appName="Translator User App" --appVersion=1.0.1 --platform=android --environment=production
```

### Optional Parameters/Flags
```sh-session
FLAGS
  -x, --extended       show extra columns
  --columns=<value>    only show provided columns (comma-separated)
  --csv                output is csv format [alias: --output=csv]
  --filter=<value>     filter property by partial string matching, ex: name=foo
  --no-header          hide table header from output
  --no-truncate        do not truncate output to fit screen
  --output=<option>    output in a more machine friendly format
                       <options: csv|json|yaml>
  --sort=<value>       property to sort by (prepend '-' for descending)
```
