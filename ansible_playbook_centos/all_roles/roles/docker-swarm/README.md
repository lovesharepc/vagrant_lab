docker-swarm
=========

設定 docker swarm 

Requirements
------------

使用 docker-ce 安裝完成 docker
ansible-galaxy collection install community.docker
pip3 install docker

client 端需安裝
/usr/libexec/platform-python -m pip install --upgrade pip
/usr/libexec/platform-python -m pip install docker

Role Variables
--------------

Dependencies
------------


Example Playbook
----------------


- name: config manager node
  hosts: all
  roles:
    - docker-swarm
  vars:
    node_role: {manager|worker}


License
-------

BSD

Author Information
------------------

   ____ __          __       _   _ 
  / __ \\ \        / //\    | \ | |　
 | |  | |\ \  /\  / //  \   |  \| |　
 | |  | | \ \/  \/ // /\ \  | . ` |_/\ 
 | |__| |  \  /\  // ____ \ | |\  |ω● |
  \____/    \/  \//_/    \_\|_| \_|￣￣