# DEnver - Docker "Environmentizer"

_Create development environments quickly using docker._

> Denver is a God. **Is God a programmer?**
> Probably not! But God automates some things.


## Dependencies

- [Docker](https://www.docker.com/)
- [PLOP](https://plopjs.com/)


## Install

Clone this repository and insert the code below into your `.bashrc` or `.zshrc`.

```shell
export DENVER_HOME="$HOME/denver"
[ -s "$DENVER_HOME/.denver/rc" ] && source $DENVER_HOME/.denver/rc
```


## Use

### Create a project

```shell
denver create <project-name> '"Project title"' '"Project description"'
```

### Update a project

```shell
denver update <project-name>
```

### Build a project

```shell
denver <project-name> build
```

### Run a project

```shell
denver <project-name>
```

### Start sshd on project

```shell
denver <project-name> start
```

### Stop sshd on project

```shell
denver <project-name> stop
```


## Know issues

### Create project with spaced string arguments

This isn't work at now:
```shell
denver create <project-name> "Project title" "Project description"
```

This work (use single and double quotes together):
```shell
denver create <project-name> '"Project title"' '"Project description"'
```
