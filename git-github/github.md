#GITHUB

##Clef SSH

https://help.github.com/en/github/authenticating-to-github/error-permission-denied-publickey

https://help.github.com/en/github/using-git/changing-a-remotes-url

https://stackoverflow.com/questions/44253270/permission-denied-publickey-when-clone-git-repo-from-bitbucket

```
ameliecuaces@yesweweb-X542UA:~/sites/lab/titre-pro/titre-pro-2020-06$ git remote -v
ameliecuaces@yesweweb-X542UA:~/sites/lab/titre-pro/titre-pro-2020-06$ ssh -T git@github.com
sign_and_send_pubkey: signing failed: agent refused operation
git@github.com: Permission denied (publickey).
ameliecuaces@yesweweb-X542UA:~/sites/lab/titre-pro/titre-pro-2020-06$ eval `ssh-agent -s`
Agent pid 20509
ameliecuaces@yesweweb-X542UA:~/sites/lab/titre-pro/titre-pro-2020-06$ ssh-add
Enter passphrase for /home/ameliecuaces/.ssh/id_rsa:
Identity added: /home/ameliecuaces/.ssh/id_rsa (ameliecuaces.dev@gmail.com)
ameliecuaces@yesweweb-X542UA:~/sites/lab/titre-pro/titre-pro-2020-06$ git clone git@github.com:melou-dev/titre-pro-2020-06.git
Cloning into 'titre-pro-2020-06'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```
