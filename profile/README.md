Gerard Braad's instant development environments
===============================================

!["Prompt"](https://raw.githubusercontent.com/gbraad/assets/gh-pages/icons/prompt-icon-64.png)

These are my instant development environments that I use for daily coding. This was originally based on C9 IDE, [published as an image](https://hub.docker.com/r/gbraad/c9ide) that got pulled over 1M+ times, and here is the article that described [how to setup a powerful self-hosted IDE in the cloud](https://gbraad.nl/blog/setting-up-a-powerful-self-hosted-ide-in-the-cloud.html). Now I focus on a reusable environment that can either be used from the command line, as a container, online deployment, editing with Vim, or easily allows you to use VSCode. But not limited to direct access, as it includes [Tailscale](https://tailscale.com) to allow [remote connectivity](https://github.com/spotsnel/tailscale-tailwings) and exposing services to other (shared) machines in the same tailnet or on the [public internet](https://tailscale.com/kb/1247/funnel-serve-use-cases/). These images are compatible with [Distrobox](https://github.com/89luca89/distrobox) and perhaps [Toolbx](https://containertoolbx.org/) (since these images rely on `sudo` there are known issues/rough edges), and can be imported to [WSL2](https://github.com/gbraad-devenv/WSL2-import) (Windows) and [Termux](https://github.com/gbraad-devenv/termux-import) (Android).

> [!NOTE]
> All images use `gbraad` as user and have [my dotfiles](https://github.com/gbraad-dotfiles/) installed. Those that are used can be listed using `devini --list`.

---


## Fedora

### [[Fedora](https://github.com/gbraad-devenv/fedora)] 41 [⚙️](https://github.com/gbraad-devenv/fedora/actions) [![build containers](https://github.com/gbraad-devenv/fedora/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/fedora/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/fedora/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/fedora/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc) - release](https://github.com/gbraad-devenv/fedora/actions/workflows/build-diskimages.yml/badge.svg)](https://github.com/gbraad-devenv/fedora/actions/workflows/build-diskimages.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=61788628&skip_quickstart=true)
  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/fedora)
  * `dev fed env`, `dev fed sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/fedora/toolbox:41 $HOSTNAME-devbox`
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/fedora/releases/tag/41)
    * `bootc switch ghcr.io/gbraad-devenv/fedora-golang/systemd-bootc:stream9`


### [[Fedora - Golang](https://github.com/gbraad-devenv/fedora-golang)] 41, with Go 1.23.4 [⚙️](https://github.com/gbraad-devenv/fedora-golang/actions) [![build containers](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-diskimages.yml/badge.svg)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-diskimages.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=914744126&skip_quickstart=true)
  * `def go run` and `def go sys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/fedora-golang/releases/tag/latest)

---


## Debian and derivatives

### [[Debian](https://github.com/gbraad-devenv/debian)] 12/Bookworm [⚙️](https://github.com/gbraad-devenv/debian/actions) [![build containers](https://github.com/gbraad-devenv/debian/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/debian/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=636945920)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/debian)
  * `dev deb env`, `dev deb sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create --init -i ghcr.io/gbraad-devenv/debian/toolbox:bookworm $HOSTNAME-debbox`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-amd64.tar.gz


### [[Debian - Golang](https://github.com/gbraad-devenv/debian-golang)] 12/Bookworm [⚙️](https://github.com/gbraad-devenv/debian-golang/actions) [![build containers](https://github.com/gbraad-devenv/debian-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/debian-golang/actions/workflows/build-containers.yml)


  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=937007673&skip_quickstart=true)
  * `dev gode env`, `dev gode sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### [[Ubuntu](https://github.com/gbraad-devenv/ubuntu)] 24.04/Noble (LTS) [⚙️](https://github.com/gbraad-devenv/ubuntu/actions) [![build containers](https://github.com/gbraad-devenv/ubuntu/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubuntu/actions/workflows/build-containers.yml)


  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubuntu)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubuntu)
  * `dev ubu env`, `dev ubu sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/ubuntu/rebase:noble devbox-ubuntu`


### [[Ubuntu - Golang](https://github.com/gbraad-devenv/ubuntu-golang)] 24.04/Noble (LTS) [⚙️](https://github.com/gbraad-devenv/ubuntu-golang/actions) [![build containers](https://github.com/gbraad-devenv/ubuntu-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubuntu-golang/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936999963&skip_quickstart=true)
  * `dev gubu env`, `dev gubu sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)

---


## EL-compatible distributions

### [[AlmaLinux](https://github.com/gbraad-devenv/almalinux)] 9 [⚙️](https://github.com/gbraad-devenv/almalinux/actions) [![build containers](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-diskimages-release.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-diskimages-release.yml)


  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/almalinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/almalinux)
  * `dev alm env`, `dev alm sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/almalinux/rebase:9 devbox-almalinux`


### [[AlmaLinux - Golang](https://github.com/gbraad-devenv/almalinux-golang)] 9, with Go 1.22.9 [⚙️](https://github.com/gbraad-devenv/almalinux-golang/actions) [![build containers](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-diskimages-release.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-diskimages-release.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=937083584&skip_quickstart=true)
  * `def goalm run` and `def goalm sys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/almalinux-golang/releases/tag/latest)
    * `bootc switch ghcr.io/gbraad-devenv/almalinux-golang/systemd-bootc:9`


### [[CentOS](https://github.com/gbraad-devenv/centos)] Stream 9 [⚙️](https://github.com/gbraad-devenv/centos/actions) [![build containers](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc) - release](https://github.com/gbraad-devenv/centos/actions/workflows/build-diskimages-release.yaml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-diskimages-release.yaml)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/centos)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/centos)
  * `dev cen env`, `dev cen sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/centos/base:stream9 devbox-centos`


### [[CentOS - Golang](https://github.com/gbraad-devenv/centos-golang)] Stream 9, with Go 1.23.4 [⚙️](https://github.com/gbraad-devenv/centos-golang/actions) [![build containers](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-diskimages.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-diskimages.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936139144&skip_quickstart=true)
  * `def gocen run` and `def gocen sys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/centos-golang/releases/tag/latest)
    * `bootc switch ghcr.io/gbraad-devenv/centos-golang/systemd-bootc:stream9`


### [[UBI](https://github.com/gbraad-devenv/ubi9)] 9 [⚙️](https://github.com/gbraad-devenv/ubi9/actions) [![build containers](https://github.com/gbraad-devenv/ubi9/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubi9/actions/workflows/build-containers.yml)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9)
  * `dev ubi env`, `dev ubi sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### [[UBI9 - Golang](https://github.com/gbraad-devenv/ubi9-golang)], with Go 1.22.9 [⚙️](https://github.com/gbraad-devenv/ubi9-golang/actions) [![build containers](https://github.com/gbraad-devenv/ubi9-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubi9-golang/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936544304&skip_quickstart=true)
  * `dev gobi env`, `dev gobi sys` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `distrobox create -i ghcr.io/gbraad-devenv/ubi9-golang/dotfiles:latest --init --name devbox-go`

---

> [!NOTE]
> Archived developer environments are [here](./archive.md).

---

## Recommended extensions
These extensions are recommended for use with these repositories for quick access within browsers and editors.

  * Gitpod
    - [Chrome extension](https://chromewebstore.google.com/detail/gitpod/dodmmooeoklaejobgleioelladacbeki)
    - [Firefox extension](https://addons.mozilla.org/en-US/firefox/addon/gitpod/)
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=gitpod.gitpod-desktop)
  * CodeSandbox
    - [Chrome extension](https://chromewebstore.google.com/detail/codesandbox/hdidglkcgdolpoijdckmafdnddjoglia)
    - [FireFox extension](https://addons.mozilla.org/en-US/firefox/addon/codesandbox/)
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=CodeSandbox-io.codesandbox-projects)
  * Tailscale
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=tailscale.vscode-tailscale)
