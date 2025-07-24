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
<!-- -->
>[!NOTE]
>Symbol to mark web external links [![alt text][1]](./README.md)
<!-- -->
>[!TIP]
>Get the link symbol with the curl command using the console
>
>>-m, --mode=MODE [![alt text][1]](https://www.man7.org/linux/man-pages/man1/mkdir.1.html) \
    set file mode (as in chmod), not a=rwx - umask
>><!-- -->
>>-p, --parents [![alt text][1]](https://www.man7.org/linux/man-pages/man1/mkdir.1.html) \
    no error if existing, make parent directories as needed,
    with their file modes unaffected by any -m option
><!-- -->
>```bash
># First make sure that the target directory exists
>mkdir -p ./img
>curl --create-dirs --output-dir img -O  "https://raw.githubusercontent.com/MathiasStadler/link_symbol_svg/360d1327d05280d53de5fa816c522f89a35891ca/img/link_symbol.svg"
>```
<!-- To comply with the format -->
FIXIT doesn't work
>[!TIP]
>Add the reference to the link image at the end of the Markdown file
<!-- -->
>```bash
># project_path.md
> printf "\n<!-- Link sign - Don't Found a better way :-( - You know a better method? - send me a email -->\n[1]: ./img/link_symbol.svg\n"  >> ./project_path.md
>#README.md
> printf "\n<!-- Link sign - Don't Found a better way :-( - You know a better method? - send me a email -->\n[1]: ./img/link_symbol.svg\n"  >> ./README.md
<!-- keep the format -->
