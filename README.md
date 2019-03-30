# Binary Downloads

## SourceForge

[![](https://img.shields.io/sourceforge/dt/hakuneko/0.4.0.svg?label=HakuNeko%200.4.0&logo=sourceforge)](https://sourceforge.net/projects/hakuneko/files/0.4.0/)

## Github

[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_macosx_amd64.dmg.svg?label=MacOSX%2064-Bit%20%28dmg%29&logo=apple&logoColor=%23a2aaad)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_macosx_amd64.dmg)

[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_linux_amd64.deb.svg?label=Linux%2064-Bit%20%28deb%29&logo=debian&logoColor=%23ce0056)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_linux_amd64.deb)<br>
[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_linux_i386.deb.svg?label=Linux%2032-Bit%20%28deb%29&logo=debian&logoColor=%23ce0056)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_linux_i386.deb)

[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_linux_amd64.rpm.svg?label=Linux%2064-Bit%20%28rpm%29&logo=linux&logoColor=green)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_linux_amd64.rpm)<br>
[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_linux_i386.rpm.svg?label=Linux%2032-Bit%20%28rpm%29&logo=linux&logoColor=green)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_linux_i386.rpm)

[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_windows-setup_amd64.exe.svg?label=Windows%2064-Bit%20Setup%20%28exe%29&logo=windows&logoColor=00a1f1)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_windows-setup_amd64.exe)<br>
[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_windows-setup_i686.exe.svg?label=Windows%2032-Bit%20Setup%20%28exe%29&logo=windows&logoColor=00a1f1)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_windows-setup_i686.exe)<br>
[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_windows-portable_amd64.zip.svg?label=Windows%2064-Bit%20Portable%20%28zip%29&logo=windows&logoColor=00a1f1)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_windows-portable_amd64.zip)<br>
[![](https://img.shields.io/github/downloads/manga-download/hakuneko/latest/hakuneko-desktop_0.4.0_windows-portable_i686.zip.svg?label=Windows%2032-Bit%20Portable%20%28zip%29&logo=windows&logoColor=00a1f1)](https://github.com/manga-download/hakuneko/releases/download/0.4.0/hakuneko-desktop_0.4.0_windows-portable_i686.zip)

# Developer Quick Start

## Introduction

*HakuNeko S* currently consists of two parts:

1. The main web-application hosted in the cloud
2. A desktop client running the web application

Both parts require `nodejs` and `npm` to be installed.

## Web-Application

The web-application is the heart of *HakuNeko S* and is written in Javascript using the polymer framework. The source files are located in the *web* sub-directory. It is recommend to install the `polymer-cli` npm package to host the web-application locally or compress the source. To host the web-application, open a terminal, change to the *web* sub-directory and run `polymer serve`. This will start a web-server hosting the web-application on *http://localhost:8081*.

Why HakuNeko became a hosted web-application?

- Manga websites are changing more frequently, the web-application can be updated and no new version needs to be downloaded and installed on the user's client
- Manga website security improvements are heavily based on Javascript, the web-application can easily understand Javascript
- Downloads with the previous version of HakuNeko were unstable, the web-application uses technology tailored for the web
- Development of connector plugins can now be done with just plain Javascript and might attract more contributers
- Minor UI changes are simpler to implement

## Desktop Client

Running the web-application in a browser only offers very limited interaction capabilities (no local file access) with the user's machine. HakuNeko offers a desktop client based on [electron](https://en.wikipedia.org/wiki/Electron_(software_framework)). The desktop client is like a tailored browser, but allows the web-application access to the file system. To develop and run the electron client, the `electron` npm package should be installed. To run the electron desktop client, open a terminal, change to the *electron* sub-directory and run `electron ./src`. The desktop client will now run the web-application hosted on *http://localhost:8081*. The *F12* key allows to open and close the developer console as in the generic chromium browser. After making changes to the source code of the web-application, press the *F5* key (while the developer console is active) to reload the web-page.
