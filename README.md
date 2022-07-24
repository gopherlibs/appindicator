# AppIndicator Go

[![Go Report Card](https://goreportcard.com/badge/github.com/gopherlibs/appindicator)](https://goreportcard.com/report/github.com/gopherlibs/appindicator)
[![GoDoc](https://godoc.org/github.com/gopherlibs/appindicator?status.svg)](https://godoc.org/github.com/gopherlibs/appindicator)
[![Mentioned in Awesome Go](https://awesome.re/mentioned-badge.svg)](https://github.com/avelino/awesome-go)

Go (golang) bindings for [libappindicator3](https://launchpad.net/libappindicator) C library.

Libappindicator is a library to allow applications to export a menu into the Unity Menu bar.
Based on KSNI it also works in KDE and will fallback to generic Systray support if none of those are available.

Also it works in:
 - Unity
 - GNOME Shell with [this extension](https://github.com/ubuntu/gnome-shell-extension-appindicator)
 - Budgie Desktop with [this applet](https://github.com/UbuntuBudgie/budgie-indicator-applet)
 - MATE with [this applet](https://github.com/mate-desktop/mate-indicator-applet)
 - Xfce with [this plugin](https://goodies.xfce.org/projects/panel-plugins/xfce4-indicator-plugin)

This package aims to be interoperable with [Go gtk3 bindings](https://github.com/gotk3/gotk3).

`3` in the name means that it's GTK3 version.

 ## Dependencies
 
On Debian-based distributions:

```bash
apt install libappindicator3-dev libgtk-3-dev
```

And of course `go` with `cgo` is required.

## Building

Refer to [gotk3 wiki](https://github.com/gotk3/gotk3/wiki)

...or simply run [`build.sh`](./build.sh) script that will try to detect
currently installed version of GTK, pass along given `go build` flags
and execute it.

For example to build one of examples:

```bash
./build.sh -v examples/simple/main.go
```

## Examples

Examples are located in [examples](./examples) directory

## Project History

AppIndicator Go is a fork of Dawid Dziurla's [go-appindicator](https://github.com/dawidd6/go-appindicator).
That project was abanzoned and eventually archived.
This project continues where that one left off, under the same MIT license (of course).
