## Registration of forgejo Runner

Refer: (https://nickcunningh.am/blog/how-to-setup-and-configure-forgejo-with-support-for-forgejo-actions-and-more#setting-up-forgejo-actions)

You would have to first uncomment below
`command: '/bin/sh -c "while : ; do sleep 1 ; done ;"'`

and then comment below
`command: '/bin/sh -c "sleep 5; forgejo-runner daemon --config /config.yaml"'`

And then follow the steps to register the runner to forgejo instance.


## Refer below for Various Github Action DIND images

```
https://nektosact.com/usage/runners.html

https://github.com/catthehacker/docker_images

https://hub.docker.com/r/catthehacker/ubuntu
```

## app.ini contains configratiton of forgejo

changing SSH_PORT modifies what you see in git clone URL while keeping ssh listen port different 

For ssh setup look below

`https://docs.codeberg.org/security/ssh-key/`


## SMTP for Forgejo

`https://resend.com/docs/send-with-smtp`


## Switch Origin

```
git remote -v
git remote set-url origin ssh://git@forgejo.0040300.xyz:222/homeden-repos/docker-compose.git
```