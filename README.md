addon (addon3) is a custom file format that i developed, first for mallet then expanded out into a multitude of my apps.
```
info {
  name myAddon
}
scripts {
  load <
    say "Hello world!"
  >
}
```
`load` being the main entry point when the addon is first loaded,
and giving addons their own .adncfg file (accessable through addon_config.yourAddonName) and a file (called disabled.adncfg) to disable addons
