---
layout: page
title: Batch Processing
permalink: /batch-processing/
nav_order: 5
parent: Modules
---

# Tesseract on 100s, 1000s of Files

```
for page in *.jpg
    do tesseract $page ${page/.jpg/} 
done
```

