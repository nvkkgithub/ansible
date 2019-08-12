Role Name
=========
'tomcat-ubuntu' role will be used to configure tomcat as a service in ubuntu environment.

Install, Uninstall, ReInstall, Start, Stop, Restart - tomcat as a service in ubuntu.
A brief description of the role goes here.

Requirements
------------
Expected Java envrionment is set.
Java is installed in '/usr/lib/java' directory.
If different, then change the path in 'defaults/main.yml' file.

Role Variables
--------------
Refer to defaults/main.yml, vars/main.yml

'action_type' - install/uninstall/reinstall/started/stopped/restarted

'java_home' - installed Java home.

'catalina_home' - target directory to install tomcat. same should be referred in 'files/tomcat.service'.

'catalina_home' - target directory to install tomcat.

'tomcat_dist_url' - Installation URL of tomcat distribution.


Dependencies
------------
NA.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------
Venkata Nidumukkala

Github: @nvkkgithub
