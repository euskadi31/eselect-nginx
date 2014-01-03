Gentoo eselect Nginx vhost module
=================================

Activate and Deactivate nginx vhost on Gentoo.

Install
-------

Copy the `nginx.eselect` file in the folder `/usr/share/eselect/modules/`

Usage
-----

Manage your nginx vhosts

~~~shell
localhost ~ # eselect nginx
Usage: eselect nginx <action> <options>

Standard actions:
  help                      Display help text
  usage                     Display usage information
  version                   Display version information

Extra actions:
  disable <target>          Disable a nginx vhost
    target                    Target name or number (from the 'list' action)
  enable <target>           Enable a nginx vhost
    target                    Target name or number (from the 'list' action)
  list                      Lists available nginx vhosts
~~~

Lists available vhost.
~~~
localhost ~ # eselect nginx list
  [1]   acme
  [2]   corporate_website *
  [3]   personal_website
  [4]   site1 *
~~~

Enable personal_website vhost
~~~shell
eselect nginx enable personal_website
~~~

Disable site1 vhost
~~~shell
eselect nginx disable site1
~~~
