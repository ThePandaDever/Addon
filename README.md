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
`load` being the main entry point when the addon is first loaded
> [!NOTE]
> Addons (unless they are loaded differently by the app) are loaded in file order, and the file's app order does not represent file order.
> Addons can also be disabled through `disabled.adncfg` (which you can just create if it does not automatically) which is a json array of names of disabled addons.

also supplying automatic file setups for `.addon` and `.adncfg` (addon config) which loads into the `addon_config` variable:
```json5
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

> [!NOTE]
> the app's save directory must be set before `addon_load_all` (simply by `save "name" "set_directory"`)
