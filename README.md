# remote-development-firebase

## Use software

- Visual Studio Code ^1.35
  - Extension: Remote - Containers
- Docker

## Start remote development

```sh
$ git clone https://github.com/inocop/remote-development-firebase.git
$ code remote-development-firebase
```

Command palette
>Remote-Containers: Reopen Folder in Container


## Create firebase project

```sh
$ pwd
/opt/remote-development-firebase

$ firebase login
# click link

$ firebase init
# select settings
```

## Run

```sh
$ firebase serve -p 5000 -o 0.0.0.0
```
