# ALiAS Blog

This repository holds the source code and related content of the official blog for Amity Linux Assitance Sapience

ALiAS is a platform for upcoming developers for finding exposure by meeting the people working in related industries, learning various languages and becoming a better developer.

The website has been created using hugo and the theme used is hugo-nederburg-theme.

This website is currently under construction and all your inputs are highly appreciated.
-   Any writers willing to add your own thoughts to the blog can refer to the "instructions for Writer" section to learn about posting on the blog.
-   Any developers interested in the development of the website can refer to the "Instructions for Developers" for help on how to contribute.
-   Anyone willing to contribute and help in this project can refer to the Issues Section of the repository and take a look at issues which they can help solve.
-   First time Git/Github users can refer to the "First time Contributors" section at the end of the document for guides and help on how to use git and Github and start contributing.

-   To be involved in the ongoing discussions please join our [Telegram Group](https://t.me/joinchat/KDFmCRdcpJrASFp5pKVaCA).

* * *

## Hugo installation and Setup

### Windows

1) Visit the link [Hugo Releases](https://github.com/gohugoio/hugo/releases) and download the latest release of hugo for Windows.(Hugo 0.53 at the time of writing this).
3) Create a directory named Hugo where you want your program to be installed.
4) Create a subdirectory bin and extract the contents of the downloaded file in that.
5) For CLI users, navigate to the location of your hugo.exe file, then add hugo.exe to PATH using the command `set PATH=%PATH%...\Hugo\bin` where ... is the path to the Hugo directory.

#### For non-CLI users:

##### For Widows 10:

1) Search and Open Advanced System Settings.
2) Click on the Environment Variables… button on the bottom.
3) In the User variables section, find the row that starts with PATH.
4) Double-click on PATH.
5) Click the New… button.
6) Type in the folder where hugo.exe was extracted.
*The PATH entry should be the folder where Hugo lives and not the binary.*

##### For Windows 7 and 8.x users:

Windows 7 and 8.1 do not include the easy path editor included in Windows 10, so non-technical users on those platforms are advised to install a free third-party path editor like Windows Environment Variables Editor or Path Editor.

* * *

### MacOS

1) Install the Homebrew utility using the command `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in macOS Terminal prompt.
2)  Install Hugo using `brew install hugo`.
3) You can check if Hugo runs corretly using `hugo version`.

* * *

### Linux

1) In any Linux Distribution that supports snap (which can be checked [here](https://docs.snapcraft.io/installing-snapd/6735)), hugo can be installed using `snap install hugo --channel=extended`.

#### Debian and Ubuntu

1)  Hugo can be installed from official Hugo debian package using `sudo apt-get install hugo`.

#### Arch Linux

1) Hugo can be installed from the Arch Linux community repository using `sudo pacman -Syu hugo`.

#### Fedora, Red Hat and CentOS

1) Hugo can be installed from official fedora package for hugo using `sudo dnf install hugo`.

#### Souls

1) Hugo can be installed from souls official repository using `sudo eopkg install hugo`.

 #### OpenBSD

 1) Hugo can be installed from its package using `doas pkg_add hugo`.



*Hugo is now installed in your sytem and is ready to use*

## Website Setup

1) clone this repository.
2) Open Terminal or your preferred CLI and navigate to the location of the repository.
3) Use the command `hugo server` to start a local sever of the website on your machine.

*The website will be available on <http://localhost:1313/>*

* * *

## Instrucitons for Developers:

`Git is required to contribute to the website and Hugo is required to run the site and test it on a local server.`

1) For hugo installation and usage instructions, refer to Hugo installation and setup Section.
2) Fork the repository to your Github account.
3) Clone the repository to your machine by using the command `git clone https://github.com/<username>/ALiAS_Blog`
4) Make the changes locally and push them to your own repository.
5) Review the changes in your repository and submit a pull request.

*hugo server starts a local server but hugo builds the website. Be careful when using the commands*

* * *

## Instruction for Writers:

*The Language used for blog posts is Markdown*

1) Fork and clone the repository. *For instructions on doing that, please refer to instructions for developers*
2) Create you work file in `/content/post`, see existing files as an example.
3)  To run a local copy of the website, open the command prompt or your preferred CLI, change the directory to the address of the repository and use the command `hugo server` if you have hugo installed.
 *For instruction on Hugo installation and use, refer to Hugo installation and setup Section.*
4)  Submit a pull request to submit your work.

 *Use /blog/images/name_of_file for your images except for the front matter where it should be /images/name_of_file and keep the images them in the images folder in static*

* * *

## First time contributors:

1) For a begineers guide on using Github, Visit [Hello World-Github](https://guides.github.com/activities/hello-world/).
2) For a guide to set up git for the first time, visit [Setting up Git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
3) For a begineers git guide, visit [git-a simple guide](http://rogerdudler.github.io/git-guide/).
4) For a detailed Git guide, you can read the book [pro git](https://git-scm.com/book/en/v2).

* * *

## Help and other Documentation:

1) *For hugo documentation, [click here](https://gohugo.io/documentation).*
2) *For markdown cheat sheet, [click here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code).*
3) *For details about the theme, [click here](https://github.com/curtistimson/hugo-theme-massively).*
4) *Getting started with ALiAS: [Getting Started](https://bit.ly/2I833jJ)*
