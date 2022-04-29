---
layout: page
title: Tesseract Basics
permalink: /tesseract-basics/
nav_order: 3
parent: Modules
---

# OCR with Tesseract

## The Basics

Tesseract's default settings are set to recognize English language, use automatic page segmentation (recognizing page format and columns), and genarate a plain text file.

The simplest way to invoke tesseract :
```
tesseract myimage.jpg myimage
```

**Example: Simple OCR**
<img alt="A Christmas Carol" src="../data/christmas-carol-pg1.jpg" width="600px"/>

Input:

```
tesseract christmas-carol-pg1.jpg christmas-carol-pg1-output
```

Result:

```
A CHRISTMAS CAROL.

STAVE I.

MARLEY’S GHOST.

Marry was dead: to begin with. There is no
doubt whatever about that. The register of his
burial was signed by the clergyman, the clerk, the
undertaker, and the chief mourner. Scrooge signed
it: and Scrooge’s name was good upon ‘Change, for
anything he chose to put his hand to. Old Marley
was as dead as a door-nail.

Mind! I don’t mean to say that I know, of my
own knowledge, what there is particularly dead
about a door-nail. I might have been inclined,
myself, to regard a coffin-nail as the deadest piece
of ironmongery in the trade. But the wisdom of

our ancestors is in the simile; and my unhallowed
B
```
