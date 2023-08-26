## Create, delete, and modify local user accounts

#### Reset the root password
- On boot screen select rescue mode. Then press `e`
- Go to the end of the line that starts with "linux"
- Add `init=/bin/bash`
- Change `ro` to `rw`
- Press `Ctrl + x` to start system
- To change the password type `passwd`
- `touch /.autorelabel`
- `exec /sbin/init`
  
## Change passwords and adjust password aging for local user accounts

## Create, delete, and modify local groups and group memberships

## Configure superuser access
