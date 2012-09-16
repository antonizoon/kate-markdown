# Markdown Syntax Highlighting for the Kate Editor

Fork of markdown syntax rules for Kate (KDE Editor) originally created by [Darrin Yeager,](http://www.dyeager.org/blog/2008/06/kate-markdown-color-syntax-highlighting.html) with improvements and updates from [claes](https://github.com/claes/kate-markdown).

I have also added my own modifications:

* This README file
* (planned) A PKGBUILD for easy installation to the system in Arch Linux
* (planned) Support for nested code highlighting using sjrd's github flavor branch

Additional contributors whose modifications have been pulled to this repository include:

* [Neamar](https://github.com/Neamar/kate-markdown) - Basic support for highlighting two-line headers.
* [Sebastien Doeraene (sjrd)](https://github.com/sjrd/kate-markdown) _ Normalized whitespace.
* [Paul Weager (metaxy)](https://github.com/metaxy/kate-markdown) - Added *.markdown to supported extensions.

## Dependencies

* KDE Desktop Environment
* Kate (Of course)

## Installing to Home Directory

    mkdir -p ~/.kde/share/apps/katepart/syntax/
    curl -L https://raw.github.com/treeofsephiroth/kate-markdown/master/markdown.xml -o ~/.kde/share/apps/katepart/syntax/markdown.xml

Then save your already opened markdown files and restart Kate.

## Installing to System Directory

Run all commands as root.

    curl -L https://raw.github.com/treeofsephiroth/kate-markdown/master/markdown.xml -o /usr/share/apps/katepart/syntax/markdown.xml
    

Then save your already opened markdown files and restart Kate.