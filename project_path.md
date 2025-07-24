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

## disable and save akt config of Visual Studio Code
```bash
mv ~/.config/Code ~/.config/Code.old
```

## list all extentions
```bash
code --list-extensions
```
## install all extentions
```bash
cat ~/.config/Code.old/extensions.list | xargs -L 1 code --install-extension
```
## remove all extentions
```bash
cat ~/.config/Code.old/extensions.list | xargs -L 1 code --uninstall-extension
```
## remove all settings
```bash
rm ~/.config/Code/User/settings.json
```
>[!NOTE]
>How to install Visual Studio Code extensions from Command line
FIXIT Missing link
https://stackoverflow.com/questions/34286515/how-to-install-visual-studio-code-extensions-from-command-line

>```bash
># code --install-extension <extension-id>
>```
## remove all keybindings 
```bash
rm ~/.config/Code/User/keybindings.json
```
## remove all snippets
```bash
rm -rf ~/.config/Code/User/snippets
```
## remove all workspace storage
```bash
rm -rf ~/.config/Code/Storage
```
## remove all workspace state
```bash
rm -rf ~/.config/Code/State
```
## remove all workspace cached data
```bash
rm -rf ~/.config/Code/CachedData
```
## remove all workspace cached extensions
```bash
rm -rf ~/.config/Code/CachedExtensions
```
## remove all workspace cached metadata
```bash
rm -rf ~/.config/Code/CachedMetadata
```
## remove all workspace cached telemetry
```bash
rm -rf ~/.config/Code/CachedTelemetry
```
## remove all workspace cached telemetry data
```bash
rm -rf ~/.config/Code/CachedTelemetryData
```
