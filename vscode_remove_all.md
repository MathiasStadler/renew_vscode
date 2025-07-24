## remove all extentions
```bash
cat ~/.config/Code.old/extensions.list | xargs -L 1 code --uninstall-extension
```
## remove all settings
```bash
rm ~/.config/Code/User/settings.json
```


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