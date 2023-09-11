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
### Get repo from remote
- Create `BaseOS.repo` and `AppStream.repo` in `/etc/yum.repos.d/` folder.
- The files should have the following structure:
```
[BaseOS]
name=BaseOS
baseurl=http://server/isorepo/BaseOS/
gpgcheck=0
metadata_expire=-1

# if there is a gpgkey given add gpgkey=...
```
- Run `dnf clean all`
- Run `dnf repolist enables`
- Run `dnf update`

### Create own repo
- `sudo subscription-manager register`
- `sudo dnf config-manager --enable AppStream`
- `sudo dnf config-manager --enable BaseOS`
- in `/etc/fstab` add `/dev/sr0        /var/www/html/isorepo   iso9660         defaults        0 0`
OR
- `mount -o loop /.../Downloads/rhel-baseos-9.0-x86_64-dvd.iso /var/www/html/isorepo`

NOTE: if using http to serve repo. Make sure httpd is enabled and firewall allows http to serve on port 80
## Modify the system bootloader
