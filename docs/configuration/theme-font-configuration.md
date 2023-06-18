# Theme and Font configuration

++ctrl+"k"++ ++ctrl+"t"++ opens the theme selector for VSCode

Or use ++spc++ ++spc++ to open the VSCode command menu, type `settings` to narrow the command list and select `Preferences: Open Settings (JSON)`.

Change the preferences for theme, font size, font family and window zoom level (size of graphical parts of the VS Code windows - positive numbers for larger, negative for smaller).

```json title=".config/Code/User/settings.json"
    "workbench.colorTheme": "Solarized Light",
    "editor.fontSize": 14,
    "editor.fontFamily": "'Fira Code', 'Ubuntu Mono', 'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'",
    "window.zoomLevel": 0,
```

++spc++ ++"f"++ ++"f"++ to save changes and apply them directly.

!!! HINT "Install fonts in the operating system"
    [Fira Code](https://github.com/tonsky/FiraCode) and [Ubuntu Mono](https://fonts.google.com/specimen/Ubuntu) fonts may require installing on your operating system.


![VSpaceCode in action](https://raw.githubusercontent.com/VSpaceCode/vspacecode.github.io/master/static/img/demo.gif)
