Gerard Braad's instant development environments
===============================================

!["Prompt"](https://raw.githubusercontent.com/gbraad/assets/gh-pages/icons/prompt-icon-64.png)

These are my instant development environments that I use for daily coding. This was originally
based on C9 IDE, [published as an image](https://hub.docker.com/r/gbraad/c9ide) that got pulled over 1M+ times, and here is the article that described [how to setup a powerful self-hosted IDE in the cloud](https://gbraad.nl/blog/setting-up-a-powerful-self-hosted-ide-in-the-cloud.html). Now I focus on a reusable environment that can either be used from the command line, as a container, online deployment, editing with Vim, or easily allows you to use VSCode. But not limited to direct access, as it includes [Tailscale](https://tailscale.com) to allow [remote connectivity](https://github.com/spotsnel/tailscale-tailwings) and exposing services to other (shared) machines in the same tailnet or on the [public internet](https://tailscale.com/kb/1247/funnel-serve-use-cases/). These images are compatible with [Toolbx](https://containertoolbx.org/) and [Distrobox](https://github.com/89luca89/distrobox) and instructions will be provided.

---

### [[Fedora](https://github.com/gbraad-devenv/fedora)]([template](https://github.com/gbraad-devenv/fedora-template)) 38

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/fedora)
  * Open in [GitHub Codespaces](https://github.com/codespaces/new?machine=standardLinux32gb&repo=61788628&ref=main&location=SouthEastAsia&devcontainer_path=.devcontainer%2Fdevcontainer.json)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/fedora)
  * `devenv` => `defenv`, `defsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[Debian](https://github.com/gbraad-devenv/debian)]([template](https://github.com/gbraad-devenv/debian-template)) 11/Bullesye

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/debian)
  * Open in [GitHub Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=636945920)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/debian)
  * `devenv` => `debenv`, `debsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[AlmaLinux](https://github.com/gbraad-devenv/almalinux)]([template](https://github.com/gbraad-devenv/almalinux-template)) 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/almalinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/almalinux)
  * `almenv`, `almsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[Alpine](https://github.com/gbraad-devenv/alpine)]([template](https://github.com/gbraad-devenv/alpine-template)) 3.18

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/alpine)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/alpine)
  * `alpenv`, `alpsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[CentOS](https://github.com/gbraad-devenv/centos)]([template](https://github.com/gbraad-devenv/centos-template)) Stream 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/centos)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/centos)
  * `cenenv`, `censys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[OpenSUSE](https://github.com/gbraad-devenv/opensuse)]([template](https://github.com/gbraad-devenv/opensuse-template)) 15.2

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/opensuse)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/opensuse)
  * `susenv`, `sussys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[RockyLinux](https://github.com/gbraad-devenv/rockylinux)]([template](https://github.com/gbraad-devenv/rockylinux-template)) 9

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/rockylinux)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/rockylinux)
  * `rocenv`, `rocsys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)


### [[Ubuntu](https://github.com/gbraad-devenv/ubuntu)]([template](https://github.com/gbraad-devenv/ubuntu-template)) 22.04/Jammy (LTS)

  * Open in [Gitpod workspace](https://gitpod.io/#https://github.com/gbraad-devenv/ubuntu)
  * Open in [CodeSandbox](https://codesandbox.io/p/github/gbraad-devenv/ubuntu)
  * `ubuenv`, `ubusys` in [my dotfiles](https://github.com/gbraad/dotfiles/blob/main/zsh/.zshrc.d/devenv.zsh)
