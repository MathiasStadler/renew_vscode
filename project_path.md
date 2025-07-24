# renew_vscode
<!-- To comply with the format -->
## Start Date of project

```bash <!-- markdownlint-disable-line code-block-style -->
$ date
Thu Jul 24 09:27:22 AM CEST 2025
```

## environment

### os
<!-- To comply with the format -->
```bash
uname -a
Linux debian 6.1.0-37-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.140-1 (2025-05-22) x86_64 GNU/Linux
```

## point release
<!-- To comply with the format -->
```bash
cat /etc/debian_version
12.11
```

## BASH version used
<!-- To comply with the format -->
```bash
echo $BASH_VERSION
5.2.15(1)-release
```

## Disable and save akt config of Visual Studio Code

```bash
mv ~/.config/Code ~/.config/Code.old
```

## List all already installed extensions

```bash
code --list-extensions
```
<!-- keep the format -->
## /w version
<!-- -->
```bash
code --list-extensions --show-versions
```
<!-- keep the format -->
>[!NOTE]
>How to install Visual Studio Code extensions from Command line
FIXIT Missing link
https://stackoverflow.com/questions/34286515/how-to-install-visual-studio-code-extensions-from-command-line

FIXIT explain example

## install extensions via command line
<!-- keep the format -->
## create extension file
<!-- keep the format -->
```bash
# code --install-extension <extension-id>
cd /tmp \
&& rm -rf /tmp/extensions.json || true \
&& cat <<EoF >/tmp/extensions.json
bierner.github-markdown-preview
bierner.markdown-checkbox
bierner.markdown-emoji
bierner.markdown-footnotes
bierner.markdown-mermaid
bierner.markdown-preview-github-styles
bierner.markdown-yaml-preamble
davidanson.vscode-markdownlint
gruntfuggly.todo-tree
holdeniscoding.vscode-list-extensions
streetsidesoftware.code-spell-checker
usernamehw.errorlens
wayou.vscode-todo-highlight
EoF
```
<!-- keep the format -->
## Install all extensions from a file as extensions list
<!-- keep the format -->
```bash
cat /tmp/extensions.json | xargs -L 1 code --install-extension
```
<!-- keep the format -->
## List installed all extensions
<!-- keep the format -->
```bash
code --list-extensions > /tmp/installed_extensions.txt
```
<!-- keep the format -->
## Uninstall all extensions
<!-- keep the format -->
```bash
cat /tmp/installed_extensions.txt | xargs -L 1 code --uninstall-extension
```
<!-- keep the format -->