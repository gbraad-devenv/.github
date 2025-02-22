Archived developer environments
===============================


## Fedora (older releases)

### [[Fedora](https://github.com/gbraad-devenv/fedora/tree/40)] 40

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=40&repo=61788628&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/40)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:40 $HOSTNAME-devbox`


> [!NOTE]
> EL10 was forked from Fedora 40


### [[Fedora](https://github.com/gbraad-devenv/fedora/tree/39)] 39

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/39)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:39 $HOSTNAME-devbox`


### [[Fedora](https://github.com/gbraad-devenv/fedora/tree/38)] 38

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/38)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:38 $HOSTNAME-devbox`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/fedora/releases/download/38/devsys-fedora-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/fedora/releases/download/38/devsys-fedora-rootfs-amd64.tar.gz

---

## Debian and derivatives

### [[Debian](https://github.com/gbraad-devenv/debian/tree/bullseye)] 11/Bullseye

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/debian/tree/bullseye)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bullseye $HOSTNAME-debbox`

> [!IMPORTANT]
> Debian Bookworm does not work on Gitpod

---

## EL-compatible distributions

### Go Toolset for [[UBI](https://github.com/gbraad-devenv/ubi9-gotoolset)] 9, with Go 1.22.7

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=904026037&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9-gotoolset)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9-gotoolset)
  * `dev gtbi env`, `dev gtbi sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### Go Toolset for [[UBI](https://github.com/gbraad-devenv/ubi8-gotoolset)] 8, with Go 1.20

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi8-gotoolset)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi8-gotoolset)

> [!NOTE]
> The image **Go Toolset for UBI 8** is not maintained anymore

### [[AlmaLinux](https://github.com/gbraad-devenv/almalinux)] 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/almalinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/almalinux)
  * `dev alm env`, `dev alm sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/almalinux/base:9 devbox-almalinux`


### [[RockyLinux](https://github.com/gbraad-devenv/rockylinux)] 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/rockylinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/rockylinux)
  * `dev roc env`, `dev roc sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/rockylinux/base:9 devbox-rockylinux`

---

## Various distributions

### [[Alpine](https://github.com/gbraad-devenv/alpine)] 3.18

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/alpine)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/alpine)
  * `dev alp env`, `dev alp sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/alpine/base:3.18 devbox-alpine`


### [[OpenSUSE](https://github.com/gbraad-devenv/opensuse)] 15.5

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/opensuse)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/opensuse)
  * `dev sus env`, `dev sus sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/opensuse/base:15.2 devbox-opensuse`


### [[Tumbleweed](https://github.com/gbraad-devenv/opensuse)] latest

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/tumbleweed)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/tumbleweed)
  * `dev tum env`, `dev tum sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/tumbleweed/base:latest devbox-tumbleweed`

> [!NOTE]
> These images are not actively maintained
