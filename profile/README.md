Gerard Braad's instant development environment containers
=========================================================

!["Prompt"](https://raw.githubusercontent.com/gbraad/assets/gh-pages/icons/prompt-icon-64.png)

These are my instant development environments that I use for daily coding. This was originally
based on C9 IDE, [published as an image](https://hub.docker.com/r/gbraad/c9ide) that got pulled over 1M+ times, and here is the article that described [how to setup a powerful self-hosted IDE in the cloud](https://gbraad.nl/blog/setting-up-a-powerful-self-hosted-ide-in-the-cloud.html). Now I focus on a reusable environment that can either be used from the command line, as a container, online deployment, editing with Vim, or easily allows you to use VSCode. But not limited to direct access, as it includes [Tailscale](https://tailscale.com) to allow [remote connectivity](https://github.com/spotsnel/tailscale-tailwings) and exposing services to other (shared) machines in the same tailnet or on the [public internet](https://tailscale.com/kb/1247/funnel-serve-use-cases/). These images are compatible with [Distrobox](https://github.com/89luca89/distrobox) and perhaps [Toolbx](https://containertoolbx.org/) (since these images rely on `sudo` there are known issues/rough edges), and can be imported to [WSL2](https://github.com/gbraad-devenv/WSL2-import) (Windows) and [Termux](https://github.com/gbraad-devenv/termux-import) (Android).

> [!NOTE]
> All images use `gbraad` as user and have [my dotfiles](https://github.com/gbraad/dotfiles/) installed. Those that are used can be listed using `devini --list`.

---

## Fedora

### [[Fedora](https://github.com/gbraad-devenv/fedora)] 41

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=61788628&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/fedora)
  * `dev fed env`, `dev fed sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:41 $HOSTNAME-devbox`
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/fedora/releases/tag/41)


### [[Fedora - Golang](https://github.com/gbraad-devenv/fedora-golang)] 41, with Go 1.23.4

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=914744126&skip_quickstart=true)
  * `def go run` and `def go sys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/fedora-golang/releases/tag/latest)


## Fedora (older releases)

### [[Fedora](https://github.com/gbraad-devenv/fedora/tree/40)] 40

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=40&repo=61788628&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/40)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:40 $HOSTNAME-devbox`


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

### [[Debian](https://github.com/gbraad-devenv/debian)] 12/Bookworm

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=636945920)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/debian)
  * `dev deb env`, `dev deb sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bookworm $HOSTNAME-debbox`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-amd64.tar.gz


### [[Debian](https://github.com/gbraad-devenv/debian/tree/bullseye)] 11/Bullseye

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/debian/tree/bullseye)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bullseye $HOSTNAME-debbox`

> [!IMPORTANT]
> Debian Bookworm does not work on Gitpod


### [[Ubuntu](https://github.com/gbraad-devenv/ubuntu)] 22.04/Jammy (LTS)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubuntu)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubuntu)
  * `dev ubu env`, `dev ubu sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/ubuntu/base:jammy devbox-ubuntu`

---

## EL-compatible distributions

### Go Toolset for [[UBI](https://github.com/gbraad-devenv/ubi9-gotoolset)] 9, with Go 1.22.7

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=904026037&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9-gotoolset)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9-gotoolset)
  * `dev gobi env`, `dev gobi sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/ubi9-gotoolset/dotfiles:1.22.7 --init --name devbox-go`


### Go Toolset for [[UBI](https://github.com/gbraad-devenv/ubi8-gotoolset)] 8, with Go 1.20

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi8-gotoolset)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi8-gotoolset)
  * `distrobox create -i ghcr.io/gbraad-devenv/ubi8-gotoolset/base:1.20 --init --name devbox-go`

> [!NOTE]
> The image **Go Toolset for UBI 8** is not maintained anymore


### [[UBI](https://github.com/gbraad-devenv/ubi9)] 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9)
  * `dev ubi env`, `dev ubi sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### [[CentOS](https://github.com/gbraad-devenv/centos)] Stream 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/centos)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/centos)
  * `dev cen env`, `dev cen sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/centos/base:stream9 devbox-centos`


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

---

## Recommended extensions
These extensions are recommended for use with these repositories for quick access within Chrome-based browsers and editors.

  * Gitpod
    - Chrome: https://chromewebstore.google.com/detail/gitpod/dodmmooeoklaejobgleioelladacbeki
    - Firefox: https://addons.mozilla.org/en-US/firefox/addon/gitpod/
    - VS Code: https://marketplace.visualstudio.com/items?itemName=gitpod.gitpod-desktop
  * CodeSandbox
    - Chrome: https://chromewebstore.google.com/detail/codesandbox/hdidglkcgdolpoijdckmafdnddjoglia
    - FireFox: https://addons.mozilla.org/en-US/firefox/addon/codesandbox/
    - VS Code: https://marketplace.visualstudio.com/items?itemName=CodeSandbox-io.codesandbox-projects
  * Tailscale
    - VS Code: https://marketplace.visualstudio.com/items?itemName=tailscale.vscode-tailscale
