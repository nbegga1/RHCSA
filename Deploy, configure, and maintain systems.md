## Schedule tasks using at and cron

## Start and stop services and configure services to start automatically at boot

## Configure systems to boot into a specific target automatically

## Configure time service clients
- `timedatectl`
- `timedatectl set-timezone <timezone>`


## Install and update software packages from Red Hat Network, a remote repository, or from the local file system
- `dnf search/info nano`
- `dnf install/remove nano`
- `dnf localinstall nano.....rpm` (local file)
- `dnf list na*`
- `dnf repolist all` & `dnf repoinfo`
- `dnf groups list` & `dnf group install "<groupname>"`
- `dnf history list` & `dnf history undo/do <history-number>`

## Modify the system bootloader
