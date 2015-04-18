# User Manuals

This repository is home to Brewtarget's user manuals. In here, you will find the source for them and the necessary instruction to build them and modify them.

## Gold Standard
Brewtarget's manual are meant to be available in multiple locales to suit the needs of our users. In order to do so, we need explicit instructions on the process to create and update them. In this project, we make use of the English locale as the "Gold Standard" and other locale as derivate works. Any non-trivial contributions to either the structure or format need to be applied to the gold standard first.

## AsciiDoc
"AsciiDoc is a human-readable document format, semantically equivalent to DocBook XML, but using plain-text mark-up conventions. AsciiDoc documents can be created using any text editor and read “as-is”, or rendered to HTML or any other format supported by a DocBook tool-chain, i.e. PDF, TeX, Unix manpages, e-books, slide presentations, etc" (Wikipedia)
For more information http://powerman.name/doc/asciidoc.

# Building manuals

## Prerequisites
* Ruby >= 2.2

## Initialization
    gem update

## Building standard formats
    rake book:build