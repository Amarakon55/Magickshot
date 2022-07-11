MagickShot – ImageMagick Screenshot
================

## Contents

-   [Usage](#usage)
-   [Dependencies](#dependencies)
    -   [Optional](#optional)
-   [Installation](#installation)
    -   [Universal](#universal)
    -   [Gentoo](#gentoo)
-   [Uninstallation](#uninstallation)
    -   [Universal](#universal-1)
    -   [Gentoo](#gentoo-1)
-   [Configuration](#configuration)

MagickShot is a program to take screenshots using ImageMagick. It is
more minimal than using scrot but more convenient than using
ImageMagick. It is the perfect balance between the two. It also supports
notification sounds.

## Usage

``` sh
`# user` magickshot --selection # take a screenshot of the selection
`# user` magickshot --window # take a screenshot of the specied window (default is focused window)
`# user` magickshot --selection --window # use the cursor to select a window to screenshot
`# user` magickshot --monitor # take a screenshot of the specified monitor (default option) (default is focused monitor, count starts from 0)
`# user` magickshot --display # take a screenshot of the entire display
```

## Dependencies

1.  imagemagick
2.  xdotool
3.  xrandr
4.  [printmon](https://github.com/amarakon/printmon)

### Optional

The following is used for notification sounds:

1.  any media player (set the `PLAYER` environment variable, the default
    is mpv)
2.  deepin-sound-theme

## Installation

### Universal

``` sh
`# user` git clone https://github.com/amarakon/magickshot
`# user` cd magickshot
`# root` make install
```

### Gentoo

``` sh
`# root` eselect repository add amarlay git https://github.com/amarakon/amarlay
`# root` emerge --sync amarlay
`# root` emerge media-gfx/magickshot
```

## Uninstallation

### Universal

``` sh
`# user` cd magickshot
`# root` make uninstall
```

### Gentoo

``` sh
`# root` emerge -c media-gfx/magickshot
# Remove my overlay (optional)
`# root` eselect-repository remove -f amarlay
`# root` emerge --sync
```

## Configuration

You can change the default options for MagickShot via the configuration
file. The configuration file is located in the configuration directory,
so usually `~/.config/magickshot/magickshot.conf`. Here is an example
configuration:

``` sh
output_directory=~/Images/Screenshots
title="%Y-%d_%R:%S"
```
