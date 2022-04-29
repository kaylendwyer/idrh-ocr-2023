---
layout: page
title: Batch Processing
permalink: /batch-processing/
nav_order: 5
parent: Modules
---

# Tesseract on 100s, 1000s of Files

The real benefit to using Tesseract over other OCR tools is the speed and ease of processing batches of files.

Basic input: 

From within the directory of files (in this case, .jpg files). For each .jpg:
- Echo the name of the file (to keep track of what is being processed)
- Instruct tesseract to run on a page, generate an image output, and apply any parameters.
- complete the loop with "done"

Input: 
```
for page in *.jpg
do 
    echo "$page"
    tesseract "$page" "$page-output" -l eng
done
```

Did it work? First check if the files have been created by listing everything in the folder:

Input:
```
ls
```

You should have a .txt file for every image file in the directory. The next step is to figure out if tesseract actually ran and wrote text to each file. Run ```head``` to check.

Input:
```
head *.txt
```

Output example:
```
==> 00000012.jpg-output.txt <==
2 A CHRISTMAS CAROL.

hands shall not disturb it, or the Country ’s done for.
You will therefore permit me to repeat, emphati-
cally, that Marley was as dead as a door-nail.

Scrooge knew he was dead? Of course he did.
How could it be otherwise? Scrooge and he were
partners for I don’t know how many years. Scrooge
was his sole executor, his sole administrator, his

==> 00000013.jpg-output.txt <==
MARLEY'S GHOST. 3

would be in any other middle-aged gentleman rashly
turning out after dark in a breezy spot—say Saint
Paul’s Churchyard for instance—literally to astonish
his son’s weak mind.

Scrooge never painted out Old Marley’s name.
There it stood, years afterwards, above the ware-
house door: Scrooge and Marley. The firm was
```

If you are running OCR on batches of random images, separate text files are useful. However, if you have a single book, you probably want the full text bundled together.

We can combine ```cat``` and an output redirect to combine the files.

Input:
```
cat *.txt > full-book-title.txt
```
If it has run correctly, there will not be any message. To check if the file has been written correctly, we can run ```cat```, ```less```, ```head```, or ```tail```. 

