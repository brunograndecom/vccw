# VCCW - Wordpress on Vagrant
## Development environment for WordPress

This is a Vagrant configuration designed for development of WordPress plugins, themes, or websites.

For full documentation go to <http://vccw.cc/>

### Installation

1. Install VirtualBox. -> https://www.virtualbox.org/
1. Install Vagrant. -> http://www.vagrantup.com/
1. Install the vagrant-hostsupdater plugin. (Optional) -> `vagrant plugin install vagrant-hostsupdater`
1. Download vagrant box -> `vagrant box add vccw-team/xenial64`
1. Copy `provision/default.yml` to `site.yml`. -> `cp provision/default.yml site.yml`
1. Edit the `site.yml`.
1. Run `vagrant up`.
1. Update hostfile (Optional) -> if record missing, than update according to site.yml
1. Open browser (default url: http://vccw.test)

### Note

* The `site.yml` has to be in the same directory with Vagrantfile.
* You can put difference to the `site.yml`.
* Admin accessible on `SITE/wp-admin` (default user: `admin`, pass: `admin`).
* If you need a dump of the database (for example to import to live site), then you can do through the `wp cli` -> `vagrant ssh && cd /var/www/html && wp db export`. The dump file can be found as `project/wordpress/*.sql`.
