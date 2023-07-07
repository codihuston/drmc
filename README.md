# Purpose

Sometimes in my developer environment, I often rerun scripts that leave containers running on a per-run basis (for debugging purposes). This means that I might end up with many containers running that I don't want to have to manually stop and remove. This script does just that, allowing you to stop and remove multiple running docker containers at once / in one command.

# Usage

> WARNING: this will forcibly remove the running docker containers you've selected.

```bash
# remove all running containers that match "syslog"
drmc syslog

Do you want to remove the following containers? (y/n)
syslog-ng_t4usqc-syslog-ng-1
syslog-ng_t4usqc-backend-1
container_dap_ci_runner_f7cf97-cucumber-run-b87595ff350e
(y/n) > y
syslog-ng_t4usqc-syslog-ng-1
syslog-ng_t4usqc-backend-1

# remove all running containers
drmc -a
```

# Installation

Add this script to your `PATH`.

If you are an administrator and want this to be available to all users,  copy this script to `/usr/local/bin`:

```
sudo mv drmc /usr/local/bin
```
