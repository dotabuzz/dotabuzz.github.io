```bash
mkdir ~/another-ssh-key && ~/cd another-ssh-key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

```bash
ssh-add ./id_rsa
```

```bash
cat id_rsa.pub
```

[Add SSH Key](https://github.com/settings/keys)

```bash
# ~/.ssh/config
Host example.com
  ForwardAgent yes
```
  
```bash
# .git/config
[remote "origin"]
        url = git@github.com:yourAccount/yourProject.git
        ...
```