# Hugo installation and Setup

## Windows (CLI Users)

1) Visit the link [Hugo Releases](https://github.com/gohugoio/hugo/releases) and download the latest release of hugo for Windows.
3) Create a directory named Hugo where you want your program to be installed.
4) Create a subdirectory bin and extract the contents of the downloaded file in that.
5) For CLI users, navigate to the location of your `hugo.exe` file, then add hugo.exe to PATH using the command 
```
set PATH=%PATH%...\Hugo\bin
``` 
**where ... is the path to the Hugo directory.**

## Windows 10 (Non-CLI Users)

1) Search and Open Advanced System Settings.
2) Click on the Environment Variables… button on the bottom.
3) In the User variables section, find the row that starts with PATH.
4) Double-click on PATH.
5) Click the New… button.
6) Type in the folder where hugo.exe was extracted.
*The PATH entry should be the folder where Hugo lives and not the binary.*

## For Windows 7 and 8.x users:

Windows 7 and 8.1 do not include the easy path editor included in Windows 10, so non-technical users on those platforms are advised to install a free third-party path editor like Windows Environment Variables Editor or Path Editor.

* * *

## MacOS

1) Install the Homebrew utility using the command in macOS Terminal prompt.

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``` 
2)  Install Hugo using `brew install hugo`.
3) You can check if Hugo runs corretly using `hugo version`.

* * *

## Linux

1) In any Linux Distribution that supports snap (which can be checked [here](https://docs.snapcraft.io/installing-snapd/6735)), hugo can be installed using 

```
$ sudo apt update
$ sudo apt install snapd
$ snap install hugo --channel=extended
```

### Debian and Ubuntu

1)  Alternatively, Hugo can be installed from official Hugo debian package using 
```
$ sudo apt-get install hugo
```

### Arch Linux

1) Hugo can be installed from the Arch Linux community repository using 
```
$ sudo pacman -Syu hugo
```

### Fedora, Red Hat and CentOS

1) Hugo can be installed from official fedora package for hugo using 
```
$ sudo dnf install hugo
```

### Souls

1) Hugo can be installed from souls official repository using 
```
$ sudo eopkg install hugo
```

### OpenBSD

 1) Hugo can be installed from its package using 
 
```
$ doas pkg_add hugo
```


*Hugo is now installed in your sytem and is ready to use*

[Go Back]()
