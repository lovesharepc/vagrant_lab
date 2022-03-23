此 LAB 建立兩個 web server
一個 DB server

另增加使用 Role 公能
及 ansible vault 保護密碼


## 說明
role 提供標準寫法讓我們可以盡量重複利用
https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html

role 不只是寫單個 tasks yaml
而是將多個 tasks yaml 依功能組合起來

比如說系統基本設定 (update、apply NTP server、set timezone ..) 屬於一個 role
安裝所需套件屬於一個 role 
更新套件屬於一個 role ....

用法為以目錄做分類
以此範例，建立三個 role 
common

D:.
├───group_vars
└───roles
    ├───common
    │   ├───handlers
    │   ├───tasks
    │   └───templates
    ├───db
    │   ├───handlers
    │   ├───tasks
    │   └───templates
    └───web
        ├───handlers
        ├───tasks
        └───templates


## 開始使用
執行 var 加密
ansible-vault encrypt group_vars/*

執行playbook 語法檢查
ansible-playbook -i hosts.yaml site.yaml --syntax-check
ansible-playbook -i hosts.yaml site.yaml --ask-vault-pass


