selinux
=========


Role Variables
--------------
#     enforcing - SELinux security policy is enforced.
#     permissive - SELinux prints warnings instead of enforcing.
#     disabled - No SELinux policy is loaded.

selinux_config: {enforcing|permissive|disabled}


how to use 
--------------

- name: apply selinux configuration to all nodes
  hosts: all
 # remote_user: root
  roles:
    - selinux
  vars: 
    selinux_config: enforcing