# pm2

Node.js Production Process Manager with a built-in Load Balancer.

- [pm2.keymetrics.io](https://pm2.keymetrics.io/){:target="_blank"}
- [github.com/Unitech/pm2](https://github.com/Unitech/pm2){:target="_blank"}

## Installation

With NPM:

```shell
npm install pm2 -g
```

## Startup Scripts Generation

PM2 can generate and configure a Startup Script to keep PM2 and your processes alive at every server restart.

```shell
# Generate Startup Script
pm2 startup

# Freeze your process list across server restart
pm2 save

# Remove Startup Script
pm2 unstartup
```

[More about Startup Scripts Generation](https://pm2.keymetrics.io/docs/usage/startup/){:target="_blank"}

## Updating PM2

```shell
# Install latest PM2 version
npm install pm2@latest -g

# Save process list, exit old PM2 & restore all processes
pm2 update
```

## Start an application

You can start any application (Node.js, Python, Ruby, binaries in $PATH...) like that:

```shell
pm2 start app.js
```

## Managing Applications

To list all running applications:

```shell
pm2 list
```

Managing apps is straightforward:

```shell
pm2 stop     <app_name|namespace|id|'all'|json_conf>
pm2 restart  <app_name|namespace|id|'all'|json_conf>
pm2 delete   <app_name|namespace|id|'all'|json_conf>
```

To have more details on a specific application:

```shell
pm2 describe <id|app_name>
```

To monitor logs, custom metrics, application information:

```shell
pm2 monit
```

[More about Process Management](https://pm2.keymetrics.io/docs/usage/process-management/){:target="_blank"}

## Cluster Mode: Node.js Load Balancing & Zero Downtime Reload

Starting a Node.js application in cluster mode that will leverage all CPUs available:

```shell
# <processes> can be 'max', -1 (all cpu minus 1) or a specified number of instances to start.
pm2 start api.js -i <processes>
```

Hot Reload allows to update an application without any downtime:

```shell
pm2 reload all
```

[More informations about how PM2 make clustering easy](https://pm2.keymetrics.io/docs/usage/cluster-mode/){:target="_blank"}
