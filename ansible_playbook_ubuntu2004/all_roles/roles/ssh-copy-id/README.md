ssh-copy-id
=========

將帳密登入的 SSH 連線
改為使用 ssh public key 登入

介紹
https://www.ssh.com/academy/ssh/copy-id

在操作的電腦產生一組 ssh key 安裝至連線的主機上當作 authorized key
如此操作就登入時就不需密碼
"passwordless logins and single sign-on using the SSH protocol"

# 步驟
## 先在本機產生SSH Key Generate an SSH Key
ssh-keygen -t rsa -b 4096 -N ''

key 位置 /root/.ssh/id_rsa
## Copy the key to a server (playbook 工作)
ssh-copy-id user@host

## 測試功能
ansible all -i hosts.yaml -m ping