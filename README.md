* sudo ln -s \`pwd\`/ansible /etc/ansible
* ls -al /etc/ansible
* cd ~/.ssh
* mkdir cosadm
* cd cosadm
* Download https://www4.stat.ncsu.edu/~tbyron/cosadm/ssh-keys.tar
* tar -xvf ~/Downloads/ssh-keys.tar
* mv .ssh/* .
* rmdir .ssh
* rm ~/Downloads/ssh-keys.tar
* sudo chown $USER:$GROUP *
* Linux machines need to have puppet config:
  <pre> profile::auth::sudoers:
        - cosadm:
          - 'ALL@NOPASSWD: ALL'</pre>
* Mac machines need to run <pre>/opt/cos/sbin/modify-sudo</pre>
