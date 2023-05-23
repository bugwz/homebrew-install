# Homebrew (un)installer

## Install Homebrew (on macOS or Linux)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

More installation information and options: <https://docs.brew.sh/Installation>.

If you are running Linux or WSL, [there are some pre-requisite packages to install](https://docs.brew.sh/Homebrew-on-Linux#requirements).

You can set `HOMEBREW_NO_INSTALL_FROM_API` to tap Homebrew/homebrew-core; by default, it will not be tapped as it is no longer necessary.

You can set `HOMEBREW_BREW_GIT_REMOTE` , `HOMEBREW_CORE_GIT_REMOTE` , `HOMEBREW_CASK_GIT_REMOTE` , `HOMEBREW_CASK_FONTS_GIT_REMOTE` , `HOMEBREW_CASK_DRIVERS_GIT_REMOTE` , `HOMEBREW_CASK_VERSIONS_GIT_REMOTE` , `HOMEBREW_BUNDLE_GIT_REMOTE` , `HOMEBREW_SERVICES_GIT_REMOTE` and `HOMEBREW_COMMAND_NOT_FOUND_GIT_REMOTE` in your shell environment to use geolocalized Git mirrors to speed up Homebrew's installation with this script and, after installation, `brew update`.

```bash
export HOMEBREW_BREW_GIT_REMOTE="..."              # put your Git mirror of Homebrew/brew here
export HOMEBREW_CORE_GIT_REMOTE="..."              # put your Git mirror of Homebrew/homebrew-core here
export HOMEBREW_CASK_GIT_REMOTE="..."              # put your Git mirror of Homebrew/homebrew-cask here
export HOMEBREW_CASK_FONTS_GIT_REMOTE="..."        # put your Git mirror of Homebrew/homebrew-cask-fonts here
export HOMEBREW_CASK_DRIVERS_GIT_REMOTE="..."      # put your Git mirror of Homebrew/homebrew-cask-drivers here
export HOMEBREW_CASK_VERSIONS_GIT_REMOTE="..."     # put your Git mirror of Homebrew/homebrew-cask-versions here
export HOMEBREW_BUNDLE_GIT_REMOTE="..."            # put your Git mirror of Homebrew/homebrew-bundle here
export HOMEBREW_SERVICES_GIT_REMOTE="..."          # put your Git mirror of Homebrew/homebrew-services here
export HOMEBREW_COMMAND_NOT_FOUND_GIT_REMOTE="..." # put your Git mirror of Homebrew/homebrew-command-not-found here here
export HOMEBREW_AUTOUPDATE_GIT_REMOTE="..."        # put your Git mirror of Homebrew/homebrew-autoupdate here here
/bin/bash -c "$(curl -fsSL https://gitee.com/bugwz/homebrew-install/raw/mirror/install.sh)"
```

The default Git remote will be used if the corresponding environment variable is unset.

If you want to run the Homebrew installer non-interactively without prompting for passwords (e.g. in automation scripts), you can use:

```bash
NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://gitee.com/bugwz/homebrew-install/raw/mirror/install.sh)"
```

## Uninstall Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://gitee.com/bugwz/homebrew-install/raw/mirror/install.sh)"
```

If you want to run the Homebrew uninstaller non-interactively, you can use:

```bash
NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://gitee.com/bugwz/homebrew-install/raw/mirror/install.sh)"
```

Download the uninstall script and run `/bin/bash uninstall.sh --help` to view more uninstall options.
