Gerard Braad's Instant Development Environments
===============================================

!["Prompt"](https://raw.githubusercontent.com/gbraad/assets/gh-pages/icons/prompt-icon-64.png)

These are my instant development environments that I use for daily coding. This was originally based on C9 IDE, [published as an image](https://hub.docker.com/r/gbraad/c9ide) that got pulled over 1M+ times, and here is the article that described [how to setup a powerful self-hosted IDE in the cloud](https://gbraad.nl/blog/setting-up-a-powerful-self-hosted-ide-in-the-cloud.html). Now I focus on a reusable environment that can either be used from the command line, as a container, online deployment, editing with Vim, or easily allows you to use VSCode. But not limited to direct access, as it includes [Tailscale](https://tailscale.com) to allow [remote connectivity](https://github.com/spotsnel/tailscale-tailwings) and exposing services to other (shared) machines in the same tailnet or on the [public internet](https://tailscale.com/kb/1247/funnel-serve-use-cases/). These images are compatible with [Distrobox](https://github.com/89luca89/distrobox) and perhaps [Toolbx](https://containertoolbx.org/) (since these images rely on `sudo` there are known issues/rough edges), and can be imported to [WSL2](https://github.com/gbraad-devenv/WSL2-import) (Windows) and [Termux](https://github.com/gbraad-devenv/termux-import) (Android).

> [!NOTE]
> All images use `gbraad` as user and have [my dotfiles](https://github.com/gbraad-dotfiles/) installed. Those that are used can be listed using `dotini devenv --list`.

---


## Fedora

### [[Fedora](https://github.com/gbraad-devenv/fedora)] 42 [⚙️](https://github.com/gbraad-devenv/fedora/actions) [![build process](https://github.com/gbraad-devenv/fedora/actions/workflows/build-process.yml/badge.svg)](https://github.com/gbraad-devenv/fedora/actions/workflows/build-process.yml) (containers, bootable containers and cloud images)

  * Containers and devcontainers
    * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=61788628&skip_quickstart=true)
    * `devenv devfedora ephemeral`, `devenv devfedora start` or `devenv ... from devfedora` in [my dotfiles](https://github.com/gbraad-dotfiles/)
    * `devbox devfedora start`, distrobox wrapper
  * Bootable Container (bootc) disk images
    * `bootc switch ghcr.io/gbraad-devenv/fedora/base-bootc:42`
    * `machine dotfedora-bootc switch devfedora`
    * `machine devfedora-bootc`
  * Cloud images
    * `machine devfedora-cloud start` or `machine ... from devfedora-cloud`


### [[Fedora - Golang](https://github.com/gbraad-devenv/fedora-golang)] 42, with Go 1.23.4 🚧 [⚙️](https://github.com/gbraad-devenv/fedora-golang/actions) [![build process](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-process.yml/badge.svg)](https://github.com/gbraad-devenv/fedora-golang/actions/workflows/build-process.yml) (containers, bootable containers and cloud images)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=914744126&skip_quickstart=true)
  * `devenv gofedora env`, `devenv gofedora start` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/fedora-golang/releases/tag/latest)
    * `bootc switch ghcr.io/gbraad-devenv/fedora-golang/systemd-bootc:41`
    * `machine golang switch`

### [[Fedora - Rust]()] 🚧


### [[Fedora - Android]()] 🚧


---


## Debian and derivatives

### [[Debian](https://github.com/gbraad-devenv/debian)] 12/Bookworm [⚙️](https://github.com/gbraad-devenv/debian/actions) [![build containers](https://github.com/gbraad-devenv/debian/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/debian/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=636945920)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/debian)
  * `devenv debian env`, `devenv debian start` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `devbox debian`
  * Termux [`./import-devsys.sh`](https://github.com/gbraad-devenv/termux-import/blob/main/import-devsys.sh) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-arm64.tar.gz
  * WSL2 [`.\import-devsys.ps1`](https://github.com/gbraad-devenv/wsl2-import/blob/main/import-devsys.ps1) https://github.com/gbraad-devenv/debian/releases/download/bookworm/devsys-debian-rootfs-amd64.tar.gz


### [[Debian - Golang](https://github.com/gbraad-devenv/debian-golang)] 12/Bookworm [⚙️](https://github.com/gbraad-devenv/debian-golang/actions) [![build containers](https://github.com/gbraad-devenv/debian-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/debian-golang/actions/workflows/build-containers.yml)


  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=937007673&skip_quickstart=true)
  * `devenv godebian env`, `devenv godebian start` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### [[Ubuntu](https://github.com/gbraad-devenv/ubuntu)] 24.04/Noble (LTS) [⚙️](https://github.com/gbraad-devenv/ubuntu/actions) [![build containers](https://github.com/gbraad-devenv/ubuntu/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubuntu/actions/workflows/build-containers.yml)


  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubuntu)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubuntu)
  * `devenv ubuntu env`, `devenv ubuntu start` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `devbox ubuntu start`


### [[Ubuntu - Golang](https://github.com/gbraad-devenv/ubuntu-golang)] 24.04/Noble (LTS) [⚙️](https://github.com/gbraad-devenv/ubuntu-golang/actions) [![build containers](https://github.com/gbraad-devenv/ubuntu-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubuntu-golang/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936999963&skip_quickstart=true)
  * `devenv goubuntu env`, `devenv goubuntu start` in [my dotfiles](https://github.com/gbraad/dotfiles/)

---


## EL-compatible distributions

### [[AlmaLinux](https://github.com/gbraad-devenv/almalinux)] 9 [⚙️](https://github.com/gbraad-devenv/almalinux/actions) [![build containers](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-diskimages-release.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux/actions/workflows/build-diskimages-release.yml)


  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/almalinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/almalinux)
  * `devenv alma env`, `devenv alma start` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `devbox alma start`


### [[AlmaLinux - Golang](https://github.com/gbraad-devenv/almalinux-golang)] 9, with Go 1.22.9 [⚙️](https://github.com/gbraad-devenv/almalinux-golang/actions) [![build containers](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-diskimages-release.yml/badge.svg)](https://github.com/gbraad-devenv/almalinux-golang/actions/workflows/build-diskimages-release.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=937083584&skip_quickstart=true)
  * `devenv goalma env` and `devenv goalma start` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/almalinux-golang/releases/tag/latest)
    * `bootc switch ghcr.io/gbraad-devenv/almalinux-golang/systemd-bootc:9`


### [[CentOS](https://github.com/gbraad-devenv/centos)] Stream 9 [⚙️](https://github.com/gbraad-devenv/centos/actions) [![build containers](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc) - release](https://github.com/gbraad-devenv/centos/actions/workflows/build-diskimages-release.yaml/badge.svg)](https://github.com/gbraad-devenv/centos/actions/workflows/build-diskimages-release.yaml)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/centos)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/centos)
  * `devenv centos env`, `dev centos start` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `devbox centos start`


### [[CentOS - Golang](https://github.com/gbraad-devenv/centos-golang)] Stream 9, with Go 1.23.4 [⚙️](https://github.com/gbraad-devenv/centos-golang/actions) [![build containers](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers.yml) [![build containers (bootc)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers-bootc.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-containers-bootc.yml) [![build diskimages (bootc)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-diskimages.yml/badge.svg)](https://github.com/gbraad-devenv/centos-golang/actions/workflows/build-diskimages.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936139144&skip_quickstart=true)
  * `devenv gocentos env` and `devenv gocentos start` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
  * Bootable Container (bootc) [disk images](https://github.com/gbraad-devenv/centos-golang/releases/tag/latest)
    * `bootc switch ghcr.io/gbraad-devenv/centos-golang/systemd-bootc:stream9`


### [[UBI](https://github.com/gbraad-devenv/ubi9)] 9 [⚙️](https://github.com/gbraad-devenv/ubi9/actions) [![build containers](https://github.com/gbraad-devenv/ubi9/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubi9/actions/workflows/build-containers.yml)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubi9)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubi9)
  * `devenv ubi9 env`, `devenv ubi9 start` in [my dotfiles](https://github.com/gbraad/dotfiles/)


### [[UBI9 - Golang](https://github.com/gbraad-devenv/ubi9-golang)], with Go 1.22.9 [⚙️](https://github.com/gbraad-devenv/ubi9-golang/actions) [![build containers](https://github.com/gbraad-devenv/ubi9-golang/actions/workflows/build-containers.yml/badge.svg)](https://github.com/gbraad-devenv/ubi9-golang/actions/workflows/build-containers.yml)

  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=936544304&skip_quickstart=true)
  * `devenv goubi env`, `devenv goubi start` in [my dotfiles](https://github.com/gbraad/dotfiles/)
  * `devbox goubi start`

---

> [!NOTE]
> Archived developer environments are [here](./archive.md).

---

## Recommended extensions
These extensions are recommended for use with these repositories for quick access within browsers and editors.

  * Dotfiles Tools
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=gbraad.dotfiles-tools) 
  * Systemd Universal Manager
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=gbraad.systemd-universal-manager)
  * Tailscale
    - [VS Code extension](https://marketplace.visualstudio.com/items?itemName=tailscale.vscode-tailscale)
