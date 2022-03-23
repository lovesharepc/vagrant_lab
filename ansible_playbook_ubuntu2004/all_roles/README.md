寫一個 role
將 ssh password login 改為
ssh key login

產生 roles 目錄結構 ansible-galaxy role init ssh-copy-id

## 開始使用
執行 var 加密
ansible-vault encrypt group_vars/*

執行playbook 語法檢查
ansible-playbook -i hosts.yaml site.yaml --syntax-check
ansible-playbook -i hosts.yaml site.yaml --ask-vault-pass


