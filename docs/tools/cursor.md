# Cursor

The AI Code Editor - https://www.cursor.com/


### Download

Download the AppImage for Linux from [https://www.cursor.com/downloads](https://www.cursor.com/downloads)

e.g. `~/Downloads/Cursor-0.47.9-x86_64.AppImage`


### Installation
Copy this AppImage to `/opt`,

```bash
sudo cp ~/Downloads/Cursor-0.47.9-x86_64.AppImage /opt/cursor.appimage
```

Make it to be executable,

```bash
sudo chmod +x /opt/cursor.appimage
```


### Desktop Icon
Create a desktop icon for Cursor,

```bash
sudo vim /usr/share/applications/cursor.desktop
```

with the following content,
```
[Desktop Entry]
Name=Cursor
Exec=/opt/cursor.appimage --no-sandbox
Icon=/opt/cursor.jpeg
Type=Application
Categories=Development;
```

Search cursor logo online, download a logo image, and copy to `/opt/cursor.jpeg`.


### Command

Create an `alias` to start Cursor from command line,

```bash
vim ~/.zshrc
```

Add this line,

```bash
alias cursor='/opt/cursor.appimage --no-sandbox'
```

Then save and source the file,

```bash
source ~/.zshrc
```
