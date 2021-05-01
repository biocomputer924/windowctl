# windowctl

# Usage
```
Usage: windowctl SP method SP [ "/" ] index

method = "get" / "insert" / "set" / "unset" / "fullscreen" / "normalize"

index = "current_desktop"
      / "current_window"
      / "desktops" [ "/" index [ "/" desktop-attribute ] ]
      / "usage"
      / "windows" [ "/" index [ "/" windows-attribute ] ]

desktop-attribute = "windows"

window-attribute = "desktop"
                 / "is_focused"
                 / "name"

window-query = *(
    "query=" window-attribute ":" value
)

example: windowctl get desktops
         windowctl insert desktops/0/windows <<< $(windowctl get current_window)
```
