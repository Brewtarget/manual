# User Manual

This repository is home to the user manual of [Brewtarget](http://www.brewtarget.org/). It is managed on [GitHub](https://github.com/Brewtarget/brewtarget) and published on [GitBook](https://www.gitbook.com/book/brewtarget/user-manual) giving anyone the ability to easily suggest modifications, correct typos, or write a translation.

## Contributions

It is important when thinking about making a contribution to have a clear intent. Identify the areas and sections you wish to modify, and keep your changes limited and focused.

Before changing anything, you will need to have a GitHub account and fork the `Brewtarget/user-manual` repository. It is on this fork that you will apply your modifications, and make the pull request.

Once you are satified with your changes, check for spelling/grammar mistake. Verify the scope of your modification, and create a pull request on the main `Brewtarget/user-manual` repository.

Come and join us writing this book.

## Gold Standard

This manual is meant to be translated in multiple locales. In order for the different versions not to look dissimilar, the `en` locale was chosen as the _Gold Standard_ of all the user manuals. This implies that other locales should aim to follow both the structure and format of the _Gold Standard_. Any major contributions, additions, and rewrites need to first be proposed on the `en` locale, and then translated.

## In-Between Publishing

This book was designed to be build and deployed through the Gitbook web platform. Due to new licensing requirements, this project is in-between publishing platform.

In the meantime, one of the easiest solution to generate the manual is through Docker.

```{bash}
# Example for the english manual.
docker run --rm -v $(pwd):/documents/ asciidoctor/docker-asciidoctor asciidoctor-pdf en/book.adoc -o build/pdf/en/brewtarget-3.0.3.pdf
# Example for the english webpage
docker run --rm -v $(pwd):/documents/ asciidoctor/docker-asciidoctor asciidoctor en/book.adoc -o build/html/en/brewtarget-3.0.3.html && cp -r en/assets build/html/en
```
