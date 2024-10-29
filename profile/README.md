Gerard Braad's instant development environment containers
=========================================================

!["Prompt"](https://raw.githubusercontent.com/gbraad/assets/gh-pages/icons/prompt-icon-64.png)

These are my instant development environments that I use for daily coding. This was originally
based on C9 IDE, [published as an image](https://hub.docker.com/r/gbraad/c9ide) that got pulled over 1M+ times, and here is the article that described [how to setup a powerful self-hosted IDE in the cloud](https://gbraad.nl/blog/setting-up-a-powerful-self-hosted-ide-in-the-cloud.html). Now I focus on a reusable environment that can either be used from the command line, as a container, online deployment, editing with Vim, or easily allows you to use VSCode. But not limited to direct access, as it includes [Tailscale](https://tailscale.com) to allow [remote connectivity](https://github.com/spotsnel/tailscale-tailwings) and exposing services to other (shared) machines in the same tailnet or on the [public internet](https://tailscale.com/kb/1247/funnel-serve-use-cases/). These images are compatible with [Distrobox](https://github.com/89luca89/distrobox) and perhaps [Toolbx](https://containertoolbx.org/) (since these images rely on `sudo` there are known issues/rough edges), and can be imported to [WSL2](https://github.com/gbraad-devenv/WSL2-import) (Windows) and [Termux](https://github.com/gbraad-devenv/termux-import) (Android).

> [!NOTE]
> All images use `gbraad` as user and have [my dotfiles](https://github.com/gbraad/dotfiles/) installed.

---

### [[Fedora](https://github.com/gbraad-devenv/fedora)]([template](https://github.com/gbraad-devenv/fedora-template)) 40

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora)
  * Open in [GitHub Codespaces](https://github.com/codespaces/new?machine=standardLinux32gb&repo=61788628&ref=main&location=SouthEastAsia&devcontainer_path=.devcontainer%2Fdevcontainer.json)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/fedora)
  * `devenv` => `defenv`, `defsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:40 $HOSTNAME-devbox`


### [[Fedora](https://github.com/gbraad-devenv/fedora)]([template](https://github.com/gbraad-devenv/fedora-template/tree/39)) 39

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/39)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:39 $HOSTNAME-devbox`


### [[Fedora](https://github.com/gbraad-devenv/fedora/tree/38)]([template](https://github.com/gbraad-devenv/fedora-template/tree/38)) 38

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora/tree/38)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:38 $HOSTNAME-devbox`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/fedora/releases/download/38/devsys-fedora-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/fedora/releases/download/38/devsys-fedora-rootfs-amd64.tar.gz


### Fedora-based [[Jupyter](https://github.com/gbraad-devenv/jupyter-fedora)]([template](https://github.com/gbraad-devenv/jupyter-fedora-template)) notebooks

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/jupyter-fedora)


### [[Debian](https://github.com/gbraad-devenv/debian)]([template](https://github.com/gbraad-devenv/debian-template)) 12/Bookworm

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=636945920)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/debian)
  * `devenv` => `debenv`, `debsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bookworm $HOSTNAME-debbox`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-amd64.tar.gz


### [[Debian](https://github.com/gbraad-devenv/debian/tree/bullseye)]([template](https://github.com/gbraad-devenv/debian-template/tree/bullseye)) 11/Bullseye

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/debian/tree/bullseye)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bullseye $HOSTNAME-debbox`


### [[AlmaLinux](https://github.com/gbraad-devenv/almalinux)]([template](https://github.com/gbraad-devenv/almalinux-template)) 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/almalinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/almalinux)
  * `almenv`, `almsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/almalinux/base:9 devbox-almalinux`


### [[Alpine](https://github.com/gbraad-devenv/alpine)]([template](https://github.com/gbraad-devenv/alpine-template)) 3.18

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/alpine)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/alpine)
  * `alpenv`, `alpsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/alpine/base:3.18 devbox-alpine`


### Go Toolset for [[UBI](https://github.com/gbraad-devenv/ubi8-gotoolset)]([template](https://github.com/gbraad-devenv/ubi8-gotoolset-template)) 8, with Go 1.20

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi8-gotoolset)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi8-gotoolset)
  * `goenv`, `gosys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/ubi8-gotoolset/base:1.20 --init --name devbox-go`


### [[UBI](https://github.com/gbraad-devenv/ubi9)]([template](https://github.com/gbraad-devenv/ubi9-template)) 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9)
  * `ubienv`, `ubisys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[CentOS](https://github.com/gbraad-devenv/centos)]([template](https://github.com/gbraad-devenv/centos-template)) Stream 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/centos)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/centos)
  * `cenenv`, `censys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/centos/base:stream9 devbox-centos`


### [[OpenSUSE](https://github.com/gbraad-devenv/opensuse)]([template](https://github.com/gbraad-devenv/opensuse-template)) 15.5

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/opensuse)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/opensuse)
  * `susenv`, `sussys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/opensuse/base:15.2 devbox-opensuse`


### [[Tumbleweed](https://github.com/gbraad-devenv/opensuse)]([template](https://github.com/gbraad-devenv/tumbleweed-template)) latest

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/tumbleweed)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/tumbleweed)
  * `tumenv`, `tumsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/tumbleweed/base:latest devbox-tumbleweed`


### [[RockyLinux](https://github.com/gbraad-devenv/rockylinux)]([template](https://github.com/gbraad-devenv/rockylinux-template)) 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/rockylinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/rockylinux)
  * `rocenv`, `rocsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/rockylinux/base:9 devbox-rockylinux`


### [[Ubuntu](https://github.com/gbraad-devenv/ubuntu)]([template](https://github.com/gbraad-devenv/ubuntu-template)) 22.04/Jammy (LTS)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubuntu)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubuntu)
  * `ubuenv`, `ubusys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * [`devbox`](https://github.com/gbraad-devenv/devbox) => `distrobox create -i ghcr.io/gbraad-devenv/ubuntu/base:jammy devbox-ubuntu`

