此 LAB 比較 include_tasks 與 import_tasks 差異

ansible 官網說明
https://docs.ansible.com/ansible/2.9/user_guide/playbooks_reuse_includes.html



## 開始使用
執行 var 加密
ansible-vault encrypt group_vars/*

執行playbook 語法檢查
ansible-playbook -i hosts.yaml site.yaml --syntax-check
ansible-playbook -i hosts.yaml site.yaml --ask-vault-pass -vv




