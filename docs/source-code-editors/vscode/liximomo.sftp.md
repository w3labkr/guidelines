# SFTP

Super fast sftp/ftp extension for VS Code.

- [github.com/liximomo/vscode-sftp](https://github.com/liximomo/vscode-sftp){:target="_blank"}

## Installation

Install through vscode extensions. Search for [SFTP](https://marketplace.visualstudio.com/items?itemName=liximomo.sftp){:target="_blank"}.

## Configuration

You can see the full config [here](https://github.com/liximomo/vscode-sftp/wiki/config){:target="_blank"}.

```json
{
    "name": "name",
    "syncMode": "full",
    "syncOption": {
        "update": true,
        "delete": true
    },
    "ignore": [
        "**/.git",
        "**/.svn",
        "**/.hg",
        "**/CVS",
        "**/.DS_Store",
        "**/Thumbs.db",
        "**/node_modules",
        "**/bower_components",
        "**/*.code-search",
        "**/.vscode", 
        "**/.history",
    ],
    "profiles": {
        "ftp": {
            "host": "127.0.0.1",
            "protocol": "ftp",
            "port": 21,
            "username": "username",
            "password": "password",
            "remotePath": "/",
            "downloadOnOpen": false,
            "uploadOnSave": true
        },
        "sftp": {
            "host": "127.0.0.1",
            "protocol": "sftp",
            "port": 22,
            "username": "username",
            "password": "password",
            "remotePath": "/",
            "privateKeyPath": "~/.ssh/id_rsa",
            "downloadOnOpen": false,
            "uploadOnSave": true
        }
    },
    "defaultProfile": "ftp",
    "$schema": "https://raw.githubusercontent.com/liximomo/vscode-sftp/master/schema/sftp.schema.json"
}
```

Context and watcher are only available at root level.

```json
{
    "watcher": {
        "files": "**/*",
        "autoUpload": true,
        "autoDelete": true
    },
}
```

## Troubleshooting

### No such file - 1.12.9

Find `options.emitClose = false;`. And add `options.autoDestroy = false;` after both instances.

```shell
$ vim ~/.vscode/extensions/liximomo.sftp-1.12.9/node_modules/ssh2-streams/lib/sftp.js
#options.emitClose = false;
options.emitClose = false; options.autoDestroy = false;
```

Relaunch visual studio code.

- [stackoverflow.com/questions/67506693/error-no-such-file-sftp-liximomo-extension](https://stackoverflow.com/questions/67506693/error-no-such-file-sftp-liximomo-extension){:target="_blank"}

### ENFILE: file table overflow

MacOS have a harsh limit on number of open files.

```shell
echo kern.maxfiles=65536 | sudo tee -a /etc/sysctl.conf
echo kern.maxfilesperproc=65536 | sudo tee -a /etc/sysctl.conf
sudo sysctl -w kern.maxfiles=65536
sudo sysctl -w kern.maxfilesperproc=65536
ulimit -n 65536
```

- [github.com/liximomo/vscode-sftp/blob/master/FAQ.md](https://github.com/liximomo/vscode-sftp/blob/master/FAQ.md){:target="_blank"}
