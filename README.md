bibLaTeX-__archaeologie__    
======= 



bibLaTeX-style for archaeologists, historians and philologists.
---
_2018/03/XX v2.3.7_


Copyright (c) 2016-2018 Lukas C. Bossert | Johannes Friedl

* Email: [info@biblatex-archaeologie.de](mailto:info@biblatex-archaeologie.de)
* Website: [www.biblatex-archaeologie.de](http://www.biblatex-archaeologie.de)

This citation-style covers the citation and bibliography rules of 
the [__German Archaeological Institute__ (DAI)](http://www.dainst.org/dai/meldungen). 
Various options are available to change and adjust 
the outcome according to one’s own preferences.
(German, English, Italian, French, Spanish)

---
*Der Stil setzt die Zitations- und Bibliographievorgaben 
des [__Deutschen Archäologischen Instituts (DAI)__ ](http://www.dainst.org/dai/meldungen) (Stand 2014) um. 
Verschiedene zusätzliche Optionen erlauben das Erscheinungsbild 
jedoch auch zu verändern, um eigenen Vorlieben anzupassen.*

---

This style contains:

documentation:

- archaeologie.pdf
- archaeologie.tex
- archaeologie-ger.pdf (*short documentation*)
- archaeologie-ger.tex

mandatory:

* archaeologie.cbx
* archaeologie.bbx
* archaeologie.dbx

language files:

- german-archaeologie.lbx
- english-archaeologie.lbx
- french-archaeologie.lbx
- italian-archaeologie.lbx
- spanish-archaeologie.lbx

additional lists and bibliographies:

- archaeologie-examples.bib
- archaeologie-lstabbrv.bib
- archaeologie-lstpublishers.bib
- archaeologie-lstlocations.bib
- archaeologie-bibcorpora.bib
- archaeologie-bibancient.bib


# Changelog

All notable changes to this project will be documented in this file.
This project **does not** adhere to [Semantic Versioning](http://semver.org/).
The markdown syntax is inspired by the conventions proposed by [keepachangelog.com](http://keepachangelog.com/).
## v2.3.7 (2018-03-XX) 

### *Added*
* New data-field `arachne = {}` to reference to the database iDAI.objects arachne


### *Changed*
* `inreferences=true` is now called `inreferencesasfullcite=true` due to better understanding of the option. There is a fallback.

### *Fixed*
* just some better coding for year delimiter (thanks to moewe!)
* 

## v2.3.6 (2018-02-20) 

### *Added*
* `citeauthorformat=firstinitialsthenfamily` as requested in
[#138](https://github.com/LukasCBossert/biblatex-archaeologie/issues/138), 
* `citeauthorformat=firstfullthenfamily` 

### *Changed*
* `jstor=false` by default, since it is no part of the guidelines
* `lstabbrv=true` by default
* `lstlocations=true` by default
* `lstpublishers=true` by default
* `citeauthorformat=firstfull` is now called `citeauthorformat=firstfulltheninitials`

### *Fixed*
* wrong entry with `\archaeologieoptions` deleted
* labeldates now work correctly


## v2.3.5 (2018-02-13) --> [current release]

### *Fixed*
* `\citereset` for author names (https://github.com/LukasCBossert/biblatex-archaeologie/issues/122)
* `\citetitle` will give the original title of a work which has the option `ancient`; 
`\citetitle*` instead will always give title without year.
* no comma before `in:` if title is missing (got wrong in last version)
* `volume`/`volumes` are now shown for `book` etc.
* `daterange` for a sequence of two years (now delimited by `\`)
* Short-journal for `Archaeologia` 
### *Changed*
* `volume` is now automatically a Roman numeral for `book`, `inbook`, `collection`, `incollection`, `proceedings`, `inproceedings`, you only insert the Arabic number.

## v2.3.4 (2017-11-19)
This update is also due to compatibility with `biblatex 3.8a`/`biber 2.8`.

### *Fixed*
* Arrangement of multiple authors with `\textcites`; see
[#115](https://github.com/LukasCBossert/biblatex-archaeologie/issues/115), solved with [https://tex.stackexchange.com/a/387162/98739](https://tex.stackexchange.com/a/387162/98739)
* Delimiter of `subtitle` and `titleaddon`, it is now a comma instead of fullstop.
* Remodelled the bibmacro `volume` and fixed a bug of a duplicate `volume`.
* `in:` is now always with minor `I` it doesn’t matter if follows a dot.


#### *added*
* `@MvBook` and its children can be listed in the bibliography together; see [#118](https://github.com/LukasCBossert/biblatex-archaeologie/issues/118)

* `\citetitle*` for showing the publication title without year of publication.

* You can use the namefield `bookauthor` now, then no *(ed.)* will be printed.


## v2.3.3 (2017-08-10) 

#### *fixed*
* typo in documentation

#### *added* 
* if there is no `translator` `\citetranslator` will fall back to the `bibstring` "owntranslation" which can be modified; see [#112](https://github.com/LukasCBossert/biblatex-archaeologie/issues/112) and [tex.stackexchange.com/q/385719/98739](https://tex.stackexchange.com/q/385719/98739) thanks to [moewe](https://tex.stackexchange.com/users/35864/moewe)

## v2.3.2 (2017-07-19)

#### *fixed*
* wrong code-example in documentation
* issue [#111](https://github.com/LukasCBossert/biblatex-archaeologie/issues/111) (regarding option `inreferences`) solved, thanks to [moewe](https://tex.stackexchange.com/users/35864/moewe)

## v2.31 (2017-05-29) 

#### *fixed*
* number after year in an article if there is no volume.
* volume and title for ancient publications

## v2.3 (2017-02-27)
#### *fixed*
* empty space deleted after bibliography entries (has only been visible when using option `seenote`)
* typo in the German documentation
* related example in German documentation corrected

#### *added* 
* get the translator of an ancient opus with `\citetranslator` or `\citetranslator*`
* more citation commands (`\smartcite`; `\autocite`; `\fullcite`; `\footfullcite`)
* support for `polyglossia`

## v2.2b (2016-10-06) 
* *typo* <br> documentation with new style

## v2.2 (2016-09-25)
* *added* <br> `uniqueme` for variant translations of ancient works.
* *added* <br> bibliography-file `archaeologie-examples.bib` included


[current release]: http://www.biblatex-archaeologie.de
[unreleased]: http://github.com/LukasCBossert/biblatex-archaeologie


______________________

This work may be distributed and/or modified under the
conditions of the LaTeX Project Public License, either version 1.3
of this license or (at your option) any later version.
The latest version of this license is in [http://www.latex-project.org/lppl.txt](http://www.latex-project.org/lppl.txt) and version 1.3 or later is part of all distributions of LaTeX
version 2005/12/01 or later.

---
This work has the LPPL maintenance status _maintained_.
The current maintainer of this work is [Lukas C. Bossert](https://github.com/LukasCBossert).

