建立 6 docker 節點
3 manager node
3 worker node

## 開始使用
執行 var 加密
ansible-vault encrypt group_vars/*

執行playbook 語法檢查
ansible-playbook -i site_dockerSwarm_hosts.yaml site_dockerSwarm_site.yaml --syntax-check
ansible-playbook -i site_dockerSwarm_hosts.yaml site_dockerSwarm_site.yaml --ask-vault-pass


