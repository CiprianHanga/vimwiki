# Awesome

### Copy config files to user's config  directory

```bash
cp /etc/xdg/awesome/rc.lua /home/user/.config/awesome/
cp /usr/share/themes/default/theme.lua /home/user/.config/awesome/
```

### Change default wallpaper

```bash
cd ~/.config/awesome
vim rc.lua
```

change:

```lua
beautiful.init(gears.filesystem.get_themes_dir() .. "default/theme.lua"
```

to:

```lua
beautiful.init("/home/ciprian/.config/awesome/theme.lua"
modkey = "Mod1"
```

then:

```bash
vim theme.lua
```

change:

```lua
theme.wallpaper = themes_path.."default/background.png"
```

to:

```lua
theme.wallpaper = "/home/user/Pictures/walls/my-wallpaper.jpg"
```

### Change Modkey

```bash
vim ~/.config/awesome/rc.lua
```

modify the line with ```modkey = "Mod4"``` to Mod1 for Alt key



