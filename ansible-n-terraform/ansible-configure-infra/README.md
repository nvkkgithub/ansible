For install/re-install/upgrade below softwares
===============================================
[] java
[] tomcat
[] nodejs

Input Params Options:
--------------------------
sw_name = java/tomcat/nodejs
action_type = install/uninstall/reinstall

Install/Uninstall Java
--------------------------
```
ansible-playbook -i inventory sw-rollout-playbook.yml -e sw_name=java -e action_type=install

ansible-playbook -i inventory sw-rollout-playbook.yml -e sw_name=java -e action_type=uninstall

```

Install Tomcat
--------------------------
```
ansible-playbook -i inventory sw-rollout-playbook.yml -e sw_name=tomcat -e action_type=install

```

Start/Stop/Restart Tomcat
--------------------------
to_state -> send this param with one of the below value.
[] reloaded
[] restarted
[] started
[] stopped

```
ansible-playbook -i inventory sw-rollout-playbook.yml -e sw_name=tomcat -e action_type=container -e to_state=started --tags to_state

```
note: above command invokes systemctl start <service>

Deploy Jenkins - Application
----------------------------
send parameter 
'deploy_jenkins=yes' and 'action_type=container'
to above command. 'to_state' is not required.
```
ansible-playbook -i inventory sw-rollout-playbook.yml -e sw_name=tomcat -e action_type=container -e --tags deploy_jenkins

```