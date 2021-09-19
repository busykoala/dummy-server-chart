# Dummy Server Chart

This is a helm chart to deploy
[dummy_server](https://github.com/busykoala/dummy_server)
using an istio gateway.

## Secure secrets with git-crypt

### Initial setup

```bash
# install git-crypt
<fav-pkg-manager-command> git-crypt

# init git-crypt in repo
# ! do not repeat after first init !
git-crypt init
```

### Usage

```bash
# add a user by key
gpg --import user_pubkey.gpg
gpg ––edit–key KJLDFUFOEJFLFE
> trust
> save
git-crypt add-gpg-user KJLDFUFOEJFLFE

# validate a files is locked
git-crypt [lock | unlock]
```

Use the `.gitattributes` file to manage encrypted files.
