# zlib.install

Windows one-line installer for zlib library.

# Usage

Open your command prompt as Administrator and enter

```
powershell -Command "(Invoke-WebRequest -Uri https://github.com/crmaxx/zlib.install/blob/master/install.bat -OutFile install_zlib.bat)"; ./install_zlib.bat; del install_zlib.bat
```

It will by default build a 64-bits library.
Set the environment variable ARCH to Win32 before-hand otherwise:

```
set ARCH=Win32
powershell -Command "(Invoke-WebRequest -Uri https://github.com/crmaxx/zlib.install/blob/master/install.bat -OutFile install_zlib.bat)"; ./install_zlib.bat; del install_zlib.bat
```

# Requirements

- Install Visual Studio with C++. Make sure to select Desktop Development with C++ while doing so.
- Make sure you have CMake: https://cmake.org/download/
- Make sure you have PowerShell: https://duckduckgo.com/?q=install+powershell+on+windows

The video https://www.youtube.com/watch?v=IsAoIqnNia4 presents a step-by-step tutorial
on how to install Visual Studio with support for C++.

# Uninstall

**!! BE CAREFUL! MAKE SURE YOU UNDERSTAND IT. !!**

Open your command prompt as Administrator and enter

```
rd /s /q "%PROGRAMFILES%"\zlib
rd /s /q "%PROGRAMFILES(X86)%\zlib"
```
