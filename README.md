addon (addon2) is a custom file format that i developed, first for mallet then expanded out into a multitude of my apps.
```yaml
info {
  name myAddon
}
scripts {
  load <
    say "Hello world!"
  >
}
```
`load` being the main entry point when the addon is first loaded (in file order, unless the app has specified otherwise / the app loads them differently and if the addon is not disabled in disabled.adncfg)

also supplying automatic file setups for `.addon` and `.adncfg` (addon config) which loads into the `addon_config` variable:
```json
{
  "myAddon":{...},
  "disabled":{...}
}
```
(for app data)
```
myAddon.adncfg
disabled.adncfg
```
