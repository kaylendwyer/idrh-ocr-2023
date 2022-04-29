---
layout: page
title: HOCR
permalink: /hocr/
nav_order: 6
parent: Modules
---
# hOCR Output

hOCR encodes the text, page layout in coordinates, and confidence intervals of text recognition into an HTML structured document. hOCR is useful when the *structure* of a document is important to data collection. 

Example use cases:
- Identifying page headers & footers for data cleaning
- Chunking and segmenting pages into words, lines, and pages for text mining
- Transferring images of tabular data to CSVs to cut back the need for manual data entry

This passenger manifest contains printed data in a tabular format. We could enter in each item manually, but hOCR enables us to read the data into a structured file. 

A possible workflow:
1. Run tesseract on the file and output to hOCR
2. Use the python library, Beautiful Soup, to parse the HTML and put it into a CSV
3. Clean the data and regularize errors (e.g., Glasgow / Glaegow) in the CSV using a tool like OpenRefine

<img alt="passenger list" src="../data/familysearch-passenger-list.jpg" width="800px"/>
Click to see full image: [1929 Massachusetts, Boston Passenger List](https://www.familysearch.org/en/wiki/Massachusetts,_Boston_Passenger_Lists,_1891-1943_-_FamilySearch_Historical_Records#/media/File:Massachusetts,_Boston_Passenger_Lists,_1891-1943_(10-0671)_DGS_5103934_208.jpg)

Input:

```
tesseract familysearch-passenger-list.jpg familysearch-passenger-list-output hocr
```

<details closed markdown="block">
<summary>Output:</summary>

```html
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
 <head>
  <title></title>
  <meta http-equiv="Content-Type" content="text/html;charset=utf-8"/>
  <meta name='ocr-system' content='tesseract v4.0.0.20190314' />
  <meta name='ocr-capabilities' content='ocr_page ocr_carea ocr_par ocr_line ocrx_word ocrp_wconf'/>
 </head>
 <body>
  <div class='ocr_page' id='page_1' title='image "familysearch-passenger-list.jpg"; bbox 0 0 1920 648; ppageno 0'>
   <div class='ocr_carea' id='block_1_1' title="bbox 636 15 937 34">
    <p class='ocr_par' id='par_1_1' lang='eng' title="bbox 636 15 937 34">
     <span class='ocr_line' id='line_1_1' title="bbox 636 15 937 34; baseline -0.033 0; x_size 20; x_descenders 5; x_ascenders 5">
      <span class='ocrx_word' id='word_1_1' title='bbox 636 21 675 34; x_wconf 91'>VISAS</span>
      <span class='ocrx_word' id='word_1_2' title='bbox 683 18 759 32; x_wconf 78'>INITIALLED</span>
      <span class='ocrx_word' id='word_1_3' title='bbox 769 17 784 29; x_wconf 96'>BY</span>
      <span class='ocrx_word' id='word_1_4' title='bbox 794 5 870 28; x_wconf 12'>TEGCHNIGAL</span>
      <span class='ocrx_word' id='word_1_5' title='bbox 879 6 937 26; x_wconf 24'>AUVIDEK</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_2' title="bbox 745 47 1866 80">
    <p class='ocr_par' id='par_1_2' lang='eng' title="bbox 745 47 1866 80">
     <span class='ocr_line' id='line_1_2' title="bbox 745 47 1866 80; baseline 0.002 -2; x_size 40.757576; x_descenders 10.189394; x_ascenders 10.189394">
      <span class='ocrx_word' id='word_1_6' title='bbox 745 47 823 78; x_wconf 96'>LIST</span>
      <span class='ocrx_word' id='word_1_7' title='bbox 836 47 892 78; x_wconf 96'>OR</span>
      <span class='ocrx_word' id='word_1_8' title='bbox 905 48 1093 80; x_wconf 96'>MANIFEST</span>
      <span class='ocrx_word' id='word_1_9' title='bbox 1105 48 1155 78; x_wconf 97'>OF</span>
      <span class='ocrx_word' id='word_1_10' title='bbox 1168 48 1279 78; x_wconf 96'>ALIEN</span>
      <span class='ocrx_word' id='word_1_11' title='bbox 1293 48 1531 79; x_wconf 96'>PASSENGERS</span>
      <span class='ocrx_word' id='word_1_12' title='bbox 1545 49 1621 80; x_wconf 96'>FOR</span>
      <span class='ocrx_word' id='word_1_13' title='bbox 1629 30 1713 80; x_wconf 96'>THE</span>
      <span class='ocrx_word' id='word_1_14' title='bbox 1726 49 1866 80; x_wconf 96'>UNITED</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_3' title="bbox 389 96 1866 132">
    <p class='ocr_par' id='par_1_3' lang='eng' title="bbox 389 96 1866 132">
     <span class='ocr_line' id='line_1_3' title="bbox 389 96 1866 113; baseline 0.001 -4; x_size 25.75; x_descenders 5.5; x_ascenders 6.75">
      <span class='ocrx_word' id='word_1_15' title='bbox 378 85 415 124; x_wconf 84'>ALL</span>
      <span class='ocrx_word' id='word_1_16' title='bbox 414 85 470 124; x_wconf 89'>ALIENS</span>
      <span class='ocrx_word' id='word_1_17' title='bbox 472 85 522 124; x_wconf 59'>arriving</span>
      <span class='ocrx_word' id='word_1_18' title='bbox 524 85 543 124; x_wconf 91'>at</span>
      <span class='ocrx_word' id='word_1_19' title='bbox 547 100 554 110; x_wconf 92'>a</span>
      <span class='ocrx_word' id='word_1_20' title='bbox 554 85 580 124; x_wconf 52'>port</span>
      <span class='ocrx_word' id='word_1_21' title='bbox 588 85 600 124; x_wconf 52'>of</span>
      <span class='ocrx_word' id='word_1_22' title='bbox 599 85 671 124; x_wconf 81'>continental</span>
      <span class='ocrx_word' id='word_1_23' title='bbox 671 85 714 124; x_wconf 85'>United</span>
      <span class='ocrx_word' id='word_1_24' title='bbox 713 85 756 124; x_wconf 71'>States</span>
      <span class='ocrx_word' id='word_1_25' title='bbox 758 85 785 124; x_wconf 71'>from</span>
      <span class='ocrx_word' id='word_1_26' title='bbox 793 101 798 109; x_wconf 96'>a</span>
      <span class='ocrx_word' id='word_1_27' title='bbox 797 85 846 124; x_wconf 52'>foreign</span>
      <span class='ocrx_word' id='word_1_28' title='bbox 846 85 876 124; x_wconf 40'>port</span>
      <span class='ocrx_word' id='word_1_29' title='bbox 879 85 904 124; x_wconf 40'>ora</span>
      <span class='ocrx_word' id='word_1_30' title='bbox 905 85 931 124; x_wconf 59'>prt</span>
      <span class='ocrx_word' id='word_1_31' title='bbox 931 85 970 124; x_wconf 59'>ofthe</span>
      <span class='ocrx_word' id='word_1_32' title='bbox 970 85 1019 124; x_wconf 55'>insular</span>
      <span class='ocrx_word' id='word_1_33' title='bbox 1022 85 1091 124; x_wconf 55'>possessions</span>
      <span class='ocrx_word' id='word_1_34' title='bbox 1093 85 1129 124; x_wconf 90'>ofthe</span>
      <span class='ocrx_word' id='word_1_35' title='bbox 1129 85 1175 124; x_wconf 86'>United</span>
      <span class='ocrx_word' id='word_1_36' title='bbox 1174 85 1219 124; x_wconf 50'>States,</span>
      <span class='ocrx_word' id='word_1_37' title='bbox 1223 85 1243 124; x_wconf 50'>and</span>
      <span class='ocrx_word' id='word_1_38' title='bbox 1243 85 1266 124; x_wconf 40'>all</span>
      <span class='ocrx_word' id='word_1_39' title='bbox 1269 85 1302 124; x_wconf 40'>aliens</span>
      <span class='ocrx_word' id='word_1_40' title='bbox 1301 85 1354 124; x_wconf 55'>arriving</span>
      <span class='ocrx_word' id='word_1_41' title='bbox 1353 85 1382 124; x_wconf 73'>ata</span>
      <span class='ocrx_word' id='word_1_42' title='bbox 1386 85 1409 124; x_wconf 49'>port</span>
      <span class='ocrx_word' id='word_1_43' title='bbox 1408 85 1425 124; x_wconf 49'>of</span>
      <span class='ocrx_word' id='word_1_44' title='bbox 1425 85 1455 124; x_wconf 56'>suid</span>
      <span class='ocrx_word' id='word_1_45' title='bbox 1460 85 1497 124; x_wconf 56'>insular</span>
      <span class='ocrx_word' id='word_1_46' title='bbox 1499 85 1568 124; x_wconf 54'>possessions</span>
      <span class='ocrx_word' id='word_1_47' title='bbox 1574 85 1601 124; x_wconf 71'>from</span>
      <span class='ocrx_word' id='word_1_48' title='bbox 1610 103 1617 111; x_wconf 91'>a</span>
      <span class='ocrx_word' id='word_1_49' title='bbox 1620 85 1663 124; x_wconf 73'>foreign</span>
      <span class='ocrx_word' id='word_1_50' title='bbox 1662 85 1695 124; x_wconf 49'>port,</span>
      <span class='ocrx_word' id='word_1_51' title='bbox 1699 102 1705 111; x_wconf 49'>a</span>
      <span class='ocrx_word' id='word_1_52' title='bbox 1711 85 1734 124; x_wconf 61'>part</span>
      <span class='ocrx_word' id='word_1_53' title='bbox 1733 85 1752 124; x_wconf 61'>of</span>
      <span class='ocrx_word' id='word_1_54' title='bbox 1753 85 1819 124; x_wconf 19'>cootinental</span>
      <span class='ocrx_word' id='word_1_55' title='bbox 1821 85 1867 124; x_wconf 78'>United</span>
     </span>
     <span class='ocr_line' id='line_1_4' title="bbox 1620 116 1866 132; baseline 0 -3; x_size 25.75; x_descenders 5.5; x_ascenders 6.75">
      <span class='ocrx_word' id='word_1_56' title='bbox 1616 105 1648 139; x_wconf 69'>This</span>
      <span class='ocrx_word' id='word_1_57' title='bbox 1654 105 1693 139; x_wconf 95'>(white)</span>
      <span class='ocrx_word' id='word_1_58' title='bbox 1698 105 1733 139; x_wconf 89'>sheet</span>
      <span class='ocrx_word' id='word_1_59' title='bbox 1737 105 1753 139; x_wconf 96'>is</span>
      <span class='ocrx_word' id='word_1_60' title='bbox 1754 105 1778 139; x_wconf 94'>for</span>
      <span class='ocrx_word' id='word_1_61' title='bbox 1777 105 1803 139; x_wconf 96'>the</span>
      <span class='ocrx_word' id='word_1_62' title='bbox 1803 105 1846 139; x_wconf 90'>listing</span>
      <span class='ocrx_word' id='word_1_63' title='bbox 1848 105 1866 139; x_wconf 90'>of</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_4' title="bbox 888 147 1289 179">
    <p class='ocr_par' id='par_1_4' lang='eng' title="bbox 888 147 1289 179">
     <span class='ocr_line' id='line_1_5' title="bbox 888 147 1289 179; baseline -0.005 -8; x_size 30; x_descenders 6; x_ascenders 10">
      <span class='ocrx_word' id='word_1_64' title='bbox 888 147 1010 177; x_wconf 96'>Passengers</span>
      <span class='ocrx_word' id='word_1_65' title='bbox 1020 147 1094 177; x_wconf 95'>sailing</span>
      <span class='ocrx_word' id='word_1_66' title='bbox 1101 147 1157 176; x_wconf 85'>from</span>
      <span class='ocrx_word' id='word_1_67' title='bbox 1164 157 1214 179; x_wconf 33'>_9</span>
      <span class='ocrx_word' id='word_1_68' title='bbox 1224 157 1271 169; x_wconf 0'>4.4.8.6.</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_5' title="bbox 1289 153 1440 176">
    <p class='ocr_par' id='par_1_5' lang='eng' title="bbox 1289 153 1440 176">
     <span class='ocr_line' id='line_1_6' title="bbox 1289 153 1440 176; baseline 0 472; x_size 30; x_descenders 7.5; x_ascenders 7.5">
      <span class='ocrx_word' id='word_1_69' title='bbox 1289 153 1440 176; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_6' title="bbox 1533 149 1845 177">
    <p class='ocr_par' id='par_1_6' lang='eng' title="bbox 1533 149 1845 177">
     <span class='ocr_line' id='line_1_7' title="bbox 1533 149 1845 177; baseline 0.006 -9; x_size 24; x_descenders 3; x_ascenders 9">
      <span class='ocrx_word' id='word_1_70' title='bbox 1533 157 1582 172; x_wconf 0'>sr</span>
      <span class='ocrx_word' id='word_1_71' title='bbox 1610 157 1714 169; x_wconf 0'>avoust</span>
      <span class='ocrx_word' id='word_1_72' title='bbox 1749 168 1755 177; x_wconf 49'>,</span>
      <span class='ocrx_word' id='word_1_73' title='bbox 1772 149 1802 174; x_wconf 67'>19</span>
      <span class='ocrx_word' id='word_1_74' title='bbox 1818 158 1845 170; x_wconf 67'>as.</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_7' title="bbox 1468 167 1745 176">
    <p class='ocr_par' id='par_1_7' lang='eng' title="bbox 1468 167 1745 176">
     <span class='ocr_line' id='line_1_8' title="bbox 1468 167 1745 176; baseline 0 -3; x_size 20; x_descenders 5; x_ascenders 5">
      <span class='ocrx_word' id='word_1_75' title='bbox 1468 167 1745 176; x_wconf 95'>  </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_8' title="bbox 0 174 1809 203">
    <p class='ocr_par' id='par_1_8' lang='eng' title="bbox 0 174 1809 203">
     <span class='ocr_line' id='line_1_9' title="bbox 0 174 1809 203; baseline 0 0; x_size 14.5; x_descenders -7.25; x_ascenders 7.25">
      <span class='ocrx_word' id='word_1_76' title='bbox 0 174 1809 203; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_9' title="bbox 0 177 1809 201">
    <p class='ocr_par' id='par_1_9' lang='eng' title="bbox 0 177 1809 201">
     <span class='ocr_line' id='line_1_10' title="bbox 0 177 1809 201; baseline 0 0; x_size 12; x_descenders -6; x_ascenders 6">
      <span class='ocrx_word' id='word_1_77' title='bbox 0 177 1809 201; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_10' title="bbox 0 177 1809 201">
    <p class='ocr_par' id='par_1_10' lang='eng' title="bbox 0 177 1809 201">
     <span class='ocr_line' id='line_1_11' title="bbox 0 177 1809 201; baseline 0 0; x_size 12; x_descenders -6; x_ascenders 6">
      <span class='ocrx_word' id='word_1_78' title='bbox 0 177 1809 201; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_11' title="bbox 0 178 1809 202">
    <p class='ocr_par' id='par_1_11' lang='eng' title="bbox 0 178 1809 202">
     <span class='ocr_line' id='line_1_12' title="bbox 0 178 1809 202; baseline 0 0; x_size 12; x_descenders -6; x_ascenders 6">
      <span class='ocrx_word' id='word_1_79' title='bbox 0 178 1809 202; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_12' title="bbox 0 181 1809 202">
    <p class='ocr_par' id='par_1_12' lang='eng' title="bbox 0 181 1809 202">
     <span class='ocr_line' id='line_1_13' title="bbox 0 181 1809 202; baseline 0 0; x_size 10.5; x_descenders -5.25; x_ascenders 5.25">
      <span class='ocrx_word' id='word_1_80' title='bbox 0 181 1809 202; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_13' title="bbox 0 181 1809 205">
    <p class='ocr_par' id='par_1_13' lang='eng' title="bbox 0 181 1809 205">
     <span class='ocr_line' id='line_1_14' title="bbox 0 181 1809 205; baseline 0 0; x_size 12; x_descenders -6; x_ascenders 6">
      <span class='ocrx_word' id='word_1_81' title='bbox 0 181 1809 205; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_14' title="bbox 208 217 1857 238">
    <p class='ocr_par' id='par_1_14' lang='eng' title="bbox 208 217 1857 238">
     <span class='ocr_line' id='line_1_15' title="bbox 208 217 1857 238; baseline 0 0; x_size 10.5; x_descenders -5.25; x_ascenders 5.25">
      <span class='ocrx_word' id='word_1_82' title='bbox 208 217 1857 238; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_15' title="bbox 208 217 1857 238">
    <p class='ocr_par' id='par_1_15' lang='eng' title="bbox 208 217 1857 238">
     <span class='ocr_line' id='line_1_16' title="bbox 208 217 1857 238; baseline 0 0; x_size 10.5; x_descenders -5.25; x_ascenders 5.25">
      <span class='ocrx_word' id='word_1_83' title='bbox 208 217 1857 238; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_16' title="bbox 208 217 1857 238">
    <p class='ocr_par' id='par_1_16' lang='eng' title="bbox 208 217 1857 238">
     <span class='ocr_line' id='line_1_17' title="bbox 208 217 1857 238; baseline 0 0; x_size 10.5; x_descenders -5.25; x_ascenders 5.25">
      <span class='ocrx_word' id='word_1_84' title='bbox 208 217 1857 238; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_17' title="bbox 208 217 1857 238">
    <p class='ocr_par' id='par_1_17' lang='eng' title="bbox 208 217 1857 238">
     <span class='ocr_line' id='line_1_18' title="bbox 208 217 1857 238; baseline 0 0; x_size 10.5; x_descenders -5.25; x_ascenders 5.25">
      <span class='ocrx_word' id='word_1_85' title='bbox 208 217 1857 238; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_18' title="bbox 208 217 1857 239">
    <p class='ocr_par' id='par_1_18' lang='eng' title="bbox 208 217 1857 239">
     <span class='ocr_line' id='line_1_19' title="bbox 208 217 1857 239; baseline 0 0; x_size 11; x_descenders -5.5; x_ascenders 5.5">
      <span class='ocrx_word' id='word_1_86' title='bbox 208 217 1857 239; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_19' title="bbox 1164 283 1224 285">
    <p class='ocr_par' id='par_1_19' lang='eng' title="bbox 1164 283 1224 285">
     <span class='ocr_line' id='line_1_20' title="bbox 1164 283 1224 285; baseline 0 0; x_size 1; x_descenders -0.5; x_ascenders 0.5">
      <span class='ocrx_word' id='word_1_87' title='bbox 1164 283 1224 285; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_20' title="bbox 874 283 883 298">
    <p class='ocr_par' id='par_1_20' lang='eng' title="bbox 874 283 883 298">
     <span class='ocr_line' id='line_1_21' title="bbox 874 283 883 298; baseline 0 350; x_size 20; x_descenders 5; x_ascenders 5">
      <span class='ocrx_word' id='word_1_88' title='bbox 874 283 883 298; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_21' title="bbox 1298 227 1299 308">
    <p class='ocr_par' id='par_1_21' lang='eng' title="bbox 1298 227 1299 308">
     <span class='ocr_line' id='line_1_22' title="bbox 1298 227 1299 308; baseline 0 0; x_size 40.5; x_descenders -20.25; x_ascenders 20.25">
      <span class='ocrx_word' id='word_1_89' title='bbox 1298 227 1299 308; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_22' title="bbox 0 3 311 338">
    <p class='ocr_par' id='par_1_22' lang='eng' title="bbox 0 3 311 338">
     <span class='ocr_line' id='line_1_23' title="bbox 0 3 311 338; baseline 0 310; x_size 140; x_descenders 35; x_ascenders 34.999996">
      <span class='ocrx_word' id='word_1_90' title='bbox 0 3 311 338; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_23' title="bbox 33 187 34 346">
    <p class='ocr_par' id='par_1_23' lang='eng' title="bbox 33 187 34 346">
     <span class='ocr_line' id='line_1_24' title="bbox 33 187 34 346; baseline 0 0; x_size 79.5; x_descenders -39.75; x_ascenders 39.75">
      <span class='ocrx_word' id='word_1_91' title='bbox 33 187 34 346; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_24' title="bbox 415 143 869 357">
    <p class='ocr_par' id='par_1_24' lang='eng' title="bbox 415 143 869 357">
     <span class='ocr_line' id='line_1_25' title="bbox 415 143 869 357; baseline 0 291; x_size 89.333328; x_descenders 22.333332; x_ascenders 22.333334">
      <span class='ocrx_word' id='word_1_92' title='bbox 415 143 869 357; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_25' title="bbox 0 355 1920 380">
    <p class='ocr_par' id='par_1_25' lang='eng' title="bbox 0 355 1920 380">
     <span class='ocr_line' id='line_1_26' title="bbox 0 355 1920 380; baseline 0 0; x_size 12.5; x_descenders -6.25; x_ascenders 6.25">
      <span class='ocrx_word' id='word_1_93' title='bbox 0 355 1920 380; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_26' title="bbox 63 357 1920 381">
    <p class='ocr_par' id='par_1_26' lang='eng' title="bbox 63 357 1920 381">
     <span class='ocr_line' id='line_1_27' title="bbox 63 357 1920 381; baseline 0 0; x_size 12; x_descenders -6; x_ascenders 6">
      <span class='ocrx_word' id='word_1_94' title='bbox 63 357 1920 381; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_27' title="bbox 90 187 93 456">
    <p class='ocr_par' id='par_1_27' lang='eng' title="bbox 90 187 93 456">
     <span class='ocr_line' id='line_1_28' title="bbox 90 187 93 456; baseline 0 0; x_size 134.5; x_descenders -67.25; x_ascenders 67.25">
      <span class='ocrx_word' id='word_1_95' title='bbox 90 187 93 456; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_28' title="bbox 511 450 522 459">
    <p class='ocr_par' id='par_1_28' lang='eng' title="bbox 511 450 522 459">
     <span class='ocr_line' id='line_1_29' title="bbox 511 450 522 459; baseline 0 189; x_size 20; x_descenders 5; x_ascenders 5">
      <span class='ocrx_word' id='word_1_96' title='bbox 511 450 522 459; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_29' title="bbox 33 189 1917 628">
    <p class='ocr_par' id='par_1_29' lang='eng' title="bbox 33 189 1917 628">
     <span class='ocr_line' id='line_1_30' title="bbox 358 189 1911 225; baseline 0.001 -9; x_size 23; x_descenders 4; x_ascenders 8">
      <span class='ocrx_word' id='word_1_97' title='bbox 358 205 364 216; x_wconf 96'>3</span>
      <span class='ocrx_word' id='word_1_98' title='bbox 911 196 912 218; x_wconf 61'>|</span>
      <span class='ocrx_word' id='word_1_99' title='bbox 957 205 964 216; x_wconf 32'>wee</span>
      <span class='ocrx_word' id='word_1_100' title='bbox 1001 194 1002 213; x_wconf 77'>|</span>
      <span class='ocrx_word' id='word_1_101' title='bbox 1042 194 1058 225; x_wconf 94'>10</span>
      <span class='ocrx_word' id='word_1_102' title='bbox 1110 197 1112 220; x_wconf 96'>|</span>
      <span class='ocrx_word' id='word_1_103' title='bbox 1199 206 1209 216; x_wconf 83'>a</span>
      <span class='ocrx_word' id='word_1_104' title='bbox 1298 195 1299 224; x_wconf 64'>]</span>
      <span class='ocrx_word' id='word_1_105' title='bbox 1341 206 1352 217; x_wconf 71'>2</span>
      <span class='ocrx_word' id='word_1_106' title='bbox 1460 194 1476 225; x_wconf 76'>13</span>
      <span class='ocrx_word' id='word_1_107' title='bbox 1607 207 1618 217; x_wconf 32'>u</span>
      <span class='ocrx_word' id='word_1_108' title='bbox 1765 207 1776 218; x_wconf 60'>8</span>
      <span class='ocrx_word' id='word_1_109' title='bbox 1893 189 1911 214; x_wconf 46'>x</span>
     </span>
     <span class='ocr_line' id='line_1_31' title="bbox 286 243 1839 271; baseline 0.001 -9; x_size 14.337377; x_descenders 3.3373766; x_ascenders 3.5649247">
      <span class='ocrx_word' id='word_1_110' title='bbox 286 252 291 266; x_wconf 77'>)</span>
      <span class='ocrx_word' id='word_1_111' title='bbox 311 251 351 262; x_wconf 84'>NAME</span>
      <span class='ocrx_word' id='word_1_112' title='bbox 358 251 371 262; x_wconf 96'>IN</span>
      <span class='ocrx_word' id='word_1_113' title='bbox 379 251 409 262; x_wconf 95'>FULL</span>
      <span class='ocrx_word' id='word_1_114' title='bbox 1001 244 1002 248; x_wconf 93'>|</span>
      <span class='ocrx_word' id='word_1_115' title='bbox 1111 243 1112 271; x_wconf 85'>|</span>
      <span class='ocrx_word' id='word_1_116' title='bbox 1170 250 1196 261; x_wconf 96'>Place</span>
      <span class='ocrx_word' id='word_1_117' title='bbox 1201 250 1211 261; x_wconf 96'>of</span>
      <span class='ocrx_word' id='word_1_118' title='bbox 1215 250 1239 261; x_wconf 95'>birth</span>
      <span class='ocrx_word' id='word_1_119' title='bbox 1390 259 1391 271; x_wconf 93'>|</span>
      <span class='ocrx_word' id='word_1_120' title='bbox 1544 250 1545 257; x_wconf 69'>|</span>
      <span class='ocrx_word' id='word_1_121' title='bbox 1696 249 1708 271; x_wconf 0'>“*</span>
      <span class='ocrx_word' id='word_1_122' title='bbox 1707 249 1731 271; x_wconf 95'>Last</span>
      <span class='ocrx_word' id='word_1_123' title='bbox 1731 249 1786 271; x_wconf 96'>permanent</span>
      <span class='ocrx_word' id='word_1_124' title='bbox 1786 249 1840 271; x_wconf 90'>residence</span>
     </span>
     <span class='ocr_line' id='line_1_32' title="bbox 927 268 1861 291; baseline 0.001 -9.004; x_size 13.033978; x_descenders 3.0339785; x_ascenders 3.2408407">
      <span class='ocrx_word' id='word_1_125' title='bbox 927 268 989 290; x_wconf 72'>‘Nationality.</span>
      <span class='ocrx_word' id='word_1_126' title='bbox 1107 269 1113 290; x_wconf 0'>TD</span>
      <span class='ocrx_word' id='word_1_127' title='bbox 1128 269 1160 290; x_wconf 0'>aiesines</span>
      <span class='ocrx_word' id='word_1_128' title='bbox 1219 269 1302 290; x_wconf 0'>pcipnaceteeaewnell</span>
      <span class='ocrx_word' id='word_1_129' title='bbox 1339 278 1364 281; x_wconf 31'>Stiles</span>
      <span class='ocrx_word' id='word_1_130' title='bbox 1390 281 1392 285; x_wconf 30'>it</span>
      <span class='ocrx_word' id='word_1_131' title='bbox 1544 273 1545 276; x_wconf 13'>]</span>
      <span class='ocrx_word' id='word_1_132' title='bbox 1662 270 1684 291; x_wconf 1'>©</span>
      <span class='ocrx_word' id='word_1_133' title='bbox 1685 270 1813 291; x_wconf 0'>aeeticeneanssnntmetinai</span>
      <span class='ocrx_word' id='word_1_134' title='bbox 1850 284 1861 286; x_wconf 26'>sl</span>
     </span>
     <span class='ocr_line' id='line_1_33' title="bbox 927 269 1912 314; baseline 0.001 -13; x_size 20.937561; x_descenders 4.9375615; x_ascenders 5">
      <span class='ocrx_word' id='word_1_135' title='bbox 927 285 990 308; x_wconf 0'>Coantey</span>
      <span class='ocrx_word' id='word_1_136' title='bbox 979 281 988 312; x_wconf 50'>of</span>
      <span class='ocrx_word' id='word_1_137' title='bbox 1013 290 1098 303; x_wconf 34'>Race</span>
      <span class='ocrx_word' id='word_1_138' title='bbox 1047 281 1060 312; x_wconf 68'>oF</span>
      <span class='ocrx_word' id='word_1_139' title='bbox 1062 290 1098 303; x_wconf 67'>people</span>
      <span class='ocrx_word' id='word_1_140' title='bbox 1111 288 1112 302; x_wconf 58'>|</span>
      <span class='ocrx_word' id='word_1_141' title='bbox 1326 282 1356 314; x_wconf 35'>a</span>
      <span class='ocrx_word' id='word_1_142' title='bbox 1390 288 1391 297; x_wconf 96'>|</span>
      <span class='ocrx_word' id='word_1_143' title='bbox 1432 282 1474 311; x_wconf 66'>Issued</span>
      <span class='ocrx_word' id='word_1_144' title='bbox 1473 282 1501 311; x_wconf 85'>at—</span>
      <span class='ocrx_word' id='word_1_145' title='bbox 1592 282 1629 311; x_wconf 94'>Date</span>
      <span class='ocrx_word' id='word_1_146' title='bbox 1895 269 1912 294; x_wconf 35'>9</span>
     </span>
     <span class='ocr_line' id='line_1_34' title="bbox 887 310 1841 338; baseline 0.005 -12; x_size 20; x_descenders 3; x_ascenders 6">
      <span class='ocrx_word' id='word_1_147' title='bbox 887 318 907 327; x_wconf 44'>Wii</span>
      <span class='ocrx_word' id='word_1_148' title='bbox 908 306 918 334; x_wconf 44'>|</span>
      <span class='ocrx_word' id='word_1_149' title='bbox 933 314 939 321; x_wconf 1'>9</span>
      <span class='ocrx_word' id='word_1_150' title='bbox 943 310 988 324; x_wconf 81'>Subject)</span>
      <span class='ocrx_word' id='word_1_151' title='bbox 1111 318 1112 326; x_wconf 63'>|</span>
      <span class='ocrx_word' id='word_1_152' title='bbox 1138 316 1177 329; x_wconf 80'>Country</span>
      <span class='ocrx_word' id='word_1_153' title='bbox 1220 316 1283 329; x_wconf 44'>City</span>
      <span class='ocrx_word' id='word_1_154' title='bbox 1240 308 1255 341; x_wconf 50'>oF</span>
      <span class='ocrx_word' id='word_1_155' title='bbox 1254 316 1282 329; x_wconf 54'>town</span>
      <span class='ocrx_word' id='word_1_156' title='bbox 1545 325 1546 328; x_wconf 68'>|</span>
      <span class='ocrx_word' id='word_1_157' title='bbox 1691 310 1731 338; x_wconf 61'>(Country</span>
      <span class='ocrx_word' id='word_1_158' title='bbox 1778 320 1841 333; x_wconf 72'>City</span>
      <span class='ocrx_word' id='word_1_159' title='bbox 1797 310 1812 338; x_wconf 83'>oF</span>
      <span class='ocrx_word' id='word_1_160' title='bbox 1813 320 1841 333; x_wconf 96'>town</span>
     </span>
     <span class='ocr_line' id='line_1_35' title="bbox 33 350 1546 367; baseline -0.001 -5; x_size 23.628012; x_descenders 5.5; x_ascenders 5.875">
      <span class='ocrx_word' id='word_1_161' title='bbox 33 350 34 362; x_wconf 87'>|</span>
      <span class='ocrx_word' id='word_1_162' title='bbox 90 354 92 367; x_wconf 94'>|</span>
      <span class='ocrx_word' id='word_1_163' title='bbox 1299 362 1300 365; x_wconf 75'>|</span>
      <span class='ocrx_word' id='word_1_164' title='bbox 1545 351 1546 360; x_wconf 79'>|</span>
     </span>
     <span class='ocr_line' id='line_1_36' title="bbox 33 371 1546 393; baseline 0.006 -9; x_size 25; x_descenders 4; x_ascenders 8">
      <span class='ocrx_word' id='word_1_165' title='bbox 33 376 34 384; x_wconf 55'>|</span>
      <span class='ocrx_word' id='word_1_166' title='bbox 91 371 92 388; x_wconf 23'>]</span>
      <span class='ocrx_word' id='word_1_167' title='bbox 1391 381 1392 386; x_wconf 85'>|</span>
      <span class='ocrx_word' id='word_1_168' title='bbox 1545 372 1546 393; x_wconf 94'>|</span>
     </span>
     <span class='ocr_line' id='line_1_37' title="bbox 91 374 1481 401; baseline 0.003 -9; x_size 19; x_descenders 3; x_ascenders 4">
      <span class='ocrx_word' id='word_1_169' title='bbox 91 389 92 392; x_wconf 89'>|</span>
      <span class='ocrx_word' id='word_1_170' title='bbox 538 374 559 401; x_wconf 48'>3)</span>
      <span class='ocrx_word' id='word_1_171' title='bbox 879 390 880 393; x_wconf 86'>|</span>
      <span class='ocrx_word' id='word_1_172' title='bbox 1299 379 1300 400; x_wconf 95'>|</span>
      <span class='ocrx_word' id='word_1_173' title='bbox 1427 382 1481 397; x_wconf 0'>fias,.J6e</span>
     </span>
     <span class='ocr_line' id='line_1_38' title="bbox 355 378 1546 418; baseline -0.009 -8.009; x_size 22; x_descenders 4; x_ascenders 7">
      <span class='ocrx_word' id='word_1_174' title='bbox 355 388 370 418; x_wconf 0'>ye</span>
      <span class='ocrx_word' id='word_1_175' title='bbox 700 396 716 407; x_wconf 7'>1</span>
      <span class='ocrx_word' id='word_1_176' title='bbox 1199 381 1217 411; x_wconf 32'>P.</span>
      <span class='ocrx_word' id='word_1_177' title='bbox 1275 402 1283 405; x_wconf 17'>a</span>
      <span class='ocrx_word' id='word_1_178' title='bbox 1419 378 1450 408; x_wconf 48'>Sie.</span>
      <span class='ocrx_word' id='word_1_179' title='bbox 1545 397 1546 400; x_wconf 96'>|</span>
     </span>
     <span class='ocr_line' id='line_1_39' title="bbox 72 390 1859 441; baseline 0.004 -24; x_size 23; x_descenders 3; x_ascenders 8">
      <span class='ocrx_word' id='word_1_180' title='bbox 72 399 92 417; x_wconf 49'>1|</span>
      <span class='ocrx_word' id='word_1_181' title='bbox 119 390 265 418; x_wconf 0'>Ze-7anderson</span>
      <span class='ocrx_word' id='word_1_182' title='bbox 335 403 354 421; x_wconf 7'>oP</span>
      <span class='ocrx_word' id='word_1_183' title='bbox 373 405 440 417; x_wconf 94'>Matilda</span>
      <span class='ocrx_word' id='word_1_184' title='bbox 451 405 506 419; x_wconf 96'>Spence</span>
      <span class='ocrx_word' id='word_1_185' title='bbox 519 400 558 422; x_wconf 1'>YAR</span>
      <span class='ocrx_word' id='word_1_186' title='bbox 586 405 603 417; x_wconf 66'>WF</span>
      <span class='ocrx_word' id='word_1_187' title='bbox 622 405 631 417; x_wconf 20'>B</span>
      <span class='ocrx_word' id='word_1_188' title='bbox 637 393 725 428; x_wconf 44'>Bervant’</span>
      <span class='ocrx_word' id='word_1_189' title='bbox 736 406 773 421; x_wconf 64'>Yes</span>
      <span class='ocrx_word' id='word_1_190' title='bbox 792 408 858 423; x_wconf 43'>English</span>
      <span class='ocrx_word' id='word_1_191' title='bbox 879 403 925 420; x_wconf 44'>Yee”</span>
      <span class='ocrx_word' id='word_1_192' title='bbox 935 408 1000 420; x_wconf 95'>Britain</span>
      <span class='ocrx_word' id='word_1_193' title='bbox 1021 401 1095 421; x_wconf 88'>Scottish</span>
      <span class='ocrx_word' id='word_1_194' title='bbox 1115 398 1190 421; x_wconf 51'>‘scotland</span>
      <span class='ocrx_word' id='word_1_195' title='bbox 1209 397 1275 421; x_wconf 68'>pate”</span>
      <span class='ocrx_word' id='word_1_196' title='bbox 1299 401 1300 413; x_wconf 88'>|</span>
      <span class='ocrx_word' id='word_1_197' title='bbox 1322 407 1378 424; x_wconf 0'>27254</span>
      <span class='ocrx_word' id='word_1_198' title='bbox 1395 399 1473 441; x_wconf 0'>&lt;Olesgee</span>
      <span class='ocrx_word' id='word_1_199' title='bbox 1545 413 1546 416; x_wconf 86'>|</span>
      <span class='ocrx_word' id='word_1_200' title='bbox 1558 405 1614 423; x_wconf 86'>9/7/29</span>
      <span class='ocrx_word' id='word_1_201' title='bbox 1671 408 1756 421; x_wconf 40'>Scotland</span>
      <span class='ocrx_word' id='word_1_202' title='bbox 1767 408 1859 421; x_wconf 87'>St.Andrews</span>
     </span>
     <span class='ocr_line' id='line_1_40' title="bbox 357 425 1482 443; baseline -0.003 0; x_size 19.937561; x_descenders 4.9375615; x_ascenders 4">
      <span class='ocrx_word' id='word_1_203' title='bbox 357 431 371 443; x_wconf 51'>y</span>
      <span class='ocrx_word' id='word_1_204' title='bbox 698 438 706 441; x_wconf 66'>=</span>
      <span class='ocrx_word' id='word_1_205' title='bbox 1112 431 1113 434; x_wconf 51'>|</span>
      <span class='ocrx_word' id='word_1_206' title='bbox 1299 426 1300 440; x_wconf 89'>|</span>
      <span class='ocrx_word' id='word_1_207' title='bbox 1436 425 1482 440; x_wconf 0'>bay</span>
     </span>
     <span class='ocr_line' id='line_1_41' title="bbox 71 427 1831 466; baseline 0.004 -12; x_size 20; x_descenders 3; x_ascenders 5">
      <span class='ocrx_word' id='word_1_208' title='bbox 71 442 78 454; x_wconf 75'>2|</span>
      <span class='ocrx_word' id='word_1_209' title='bbox 115 439 159 458; x_wconf 58'>Jaw</span>
      <span class='ocrx_word' id='word_1_210' title='bbox 183 443 233 458; x_wconf 39'>Byrne</span>
      <span class='ocrx_word' id='word_1_211' title='bbox 341 443 358 459; x_wconf 23'>ff</span>
      <span class='ocrx_word' id='word_1_212' title='bbox 373 444 410 459; x_wconf 87'>Mary</span>
      <span class='ocrx_word' id='word_1_213' title='bbox 522 435 554 464; x_wconf 57'>Yes</span>
      <span class='ocrx_word' id='word_1_214' title='bbox 573 431 632 461; x_wconf 44'>view</span>
      <span class='ocrx_word' id='word_1_215' title='bbox 648 428 696 465; x_wconf 0'>aize°</span>
      <span class='ocrx_word' id='word_1_216' title='bbox 731 427 750 465; x_wconf 19'>/;</span>
      <span class='ocrx_word' id='word_1_217' title='bbox 745 445 772 458; x_wconf 80'>Yeg</span>
      <span class='ocrx_word' id='word_1_218' title='bbox 793 445 858 460; x_wconf 94'>English</span>
      <span class='ocrx_word' id='word_1_219' title='bbox 879 429 880 452; x_wconf 79'>|</span>
      <span class='ocrx_word' id='word_1_220' title='bbox 887 444 915 458; x_wconf 51'>ved</span>
      <span class='ocrx_word' id='word_1_221' title='bbox 935 445 1000 457; x_wconf 96'>Britain</span>
      <span class='ocrx_word' id='word_1_222' title='bbox 1021 446 1094 458; x_wconf 96'>Scottish</span>
      <span class='ocrx_word' id='word_1_223' title='bbox 1112 446 1190 462; x_wconf 27'>[Scotland</span>
      <span class='ocrx_word' id='word_1_224' title='bbox 1209 446 1275 461; x_wconf 28'>Glasgow</span>
      <span class='ocrx_word' id='word_1_225' title='bbox 1299 454 1301 460; x_wconf 95'>|</span>
      <span class='ocrx_word' id='word_1_226' title='bbox 1314 442 1378 457; x_wconf 60'>“14677</span>
      <span class='ocrx_word' id='word_1_227' title='bbox 1383 438 1398 466; x_wconf 89'>|</span>
      <span class='ocrx_word' id='word_1_228' title='bbox 1407 445 1473 460; x_wconf 94'>Glasgow</span>
      <span class='ocrx_word' id='word_1_229' title='bbox 1548 438 1614 466; x_wconf 73'>25/4/29</span>
      <span class='ocrx_word' id='word_1_230' title='bbox 1667 443 1757 458; x_wconf 65'>Scotland</span>
      <span class='ocrx_word' id='word_1_231' title='bbox 1766 446 1831 461; x_wconf 96'>Glasgow</span>
     </span>
     <span class='ocr_line' id='line_1_42' title="bbox 91 463 1481 483; baseline -0.001 -5; x_size 19; x_descenders 5; x_ascenders 3">
      <span class='ocrx_word' id='word_1_232' title='bbox 91 465 92 483; x_wconf 92'>|</span>
      <span class='ocrx_word' id='word_1_233' title='bbox 144 473 165 478; x_wconf 45'>—</span>
      <span class='ocrx_word' id='word_1_234' title='bbox 516 472 517 475; x_wconf 35'>)</span>
      <span class='ocrx_word' id='word_1_235' title='bbox 879 470 880 481; x_wconf 80'>|</span>
      <span class='ocrx_word' id='word_1_236' title='bbox 1418 463 1440 478; x_wconf 59'>Ke</span>
      <span class='ocrx_word' id='word_1_237' title='bbox 1449 465 1481 477; x_wconf 11'>bv</span>
     </span>
     <span class='ocr_line' id='line_1_43' title="bbox 71 472 1831 531; baseline 0.003 -38; x_size 21; x_descenders 3; x_ascenders 6">
      <span class='ocrx_word' id='word_1_238' title='bbox 71 480 78 492; x_wconf 81'>3</span>
      <span class='ocrx_word' id='word_1_239' title='bbox 91 484 118 498; x_wconf 1'>|Z</span>
      <span class='ocrx_word' id='word_1_240' title='bbox 133 475 180 497; x_wconf 26'>4a,</span>
      <span class='ocrx_word' id='word_1_241' title='bbox 182 481 233 496; x_wconf 86'>Byrne</span>
      <span class='ocrx_word' id='word_1_242' title='bbox 343 476 369 500; x_wconf 1'>pf”</span>
      <span class='ocrx_word' id='word_1_243' title='bbox 372 482 420 497; x_wconf 88'>Agnes</span>
      <span class='ocrx_word' id='word_1_244' title='bbox 509 476 532 531; x_wconf 50'>If</span>
      <span class='ocrx_word' id='word_1_245' title='bbox 546 472 631 496; x_wconf 0'>a4y¥inis</span>
      <span class='ocrx_word' id='word_1_246' title='bbox 650 482 678 495; x_wconf 68'>wir</span>
      <span class='ocrx_word' id='word_1_247' title='bbox 745 483 763 495; x_wconf 34'>No)</span>
      <span class='ocrx_word' id='word_1_248' title='bbox 792 482 821 494; x_wconf 69'>Wil</span>
      <span class='ocrx_word' id='word_1_249' title='bbox 879 482 905 497; x_wconf 50'>|Mo</span>
      <span class='ocrx_word' id='word_1_250' title='bbox 935 482 1001 495; x_wconf 95'>Britain</span>
      <span class='ocrx_word' id='word_1_251' title='bbox 1021 483 1095 496; x_wconf 95'>Scottish</span>
      <span class='ocrx_word' id='word_1_252' title='bbox 1112 484 1190 496; x_wconf 92'>Scotland</span>
      <span class='ocrx_word' id='word_1_253' title='bbox 1200 480 1274 498; x_wconf 60'>Glasgow</span>
      <span class='ocrx_word' id='word_1_254' title='bbox 1312 483 1324 498; x_wconf 36'>/</span>
      <span class='ocrx_word' id='word_1_255' title='bbox 1333 484 1378 496; x_wconf 83'>14678</span>
      <span class='ocrx_word' id='word_1_256' title='bbox 1407 482 1470 498; x_wconf 89'>Glasgow</span>
      <span class='ocrx_word' id='word_1_257' title='bbox 1549 480 1614 498; x_wconf 73'>25/4/29</span>
      <span class='ocrx_word' id='word_1_258' title='bbox 1666 481 1757 496; x_wconf 53'>“Scotland</span>
      <span class='ocrx_word' id='word_1_259' title='bbox 1766 483 1831 498; x_wconf 95'>Glasgow</span>
     </span>
     <span class='ocr_line' id='line_1_44' title="bbox 91 494 1547 526; baseline 0.002 -13; x_size 23.628012; x_descenders 5.5; x_ascenders 5.875">
      <span class='ocrx_word' id='word_1_260' title='bbox 91 499 92 510; x_wconf 11'>\,</span>
      <span class='ocrx_word' id='word_1_261' title='bbox 879 504 880 508; x_wconf 82'>|</span>
      <span class='ocrx_word' id='word_1_262' title='bbox 1200 508 1201 519; x_wconf 93'>|</span>
      <span class='ocrx_word' id='word_1_263' title='bbox 1300 506 1301 510; x_wconf 93'>|</span>
      <span class='ocrx_word' id='word_1_264' title='bbox 1421 494 1446 526; x_wconf 55'>he,</span>
      <span class='ocrx_word' id='word_1_265' title='bbox 1452 504 1482 516; x_wconf 23'>bw</span>
      <span class='ocrx_word' id='word_1_266' title='bbox 1546 517 1547 521; x_wconf 87'>|</span>
     </span>
     <span class='ocr_line' id='line_1_45' title="bbox 71 504 1907 540; baseline 0.002 -9; x_size 20; x_descenders 3; x_ascenders 5">
      <span class='ocrx_word' id='word_1_267' title='bbox 71 518 78 529; x_wconf 67'>4</span>
      <span class='ocrx_word' id='word_1_268' title='bbox 91 513 121 531; x_wconf 3'>|e</span>
      <span class='ocrx_word' id='word_1_269' title='bbox 132 509 157 539; x_wconf 37'>Gag</span>
      <span class='ocrx_word' id='word_1_270' title='bbox 182 520 233 534; x_wconf 86'>Byrne</span>
      <span class='ocrx_word' id='word_1_271' title='bbox 345 504 374 540; x_wconf 14'>mae</span>
      <span class='ocrx_word' id='word_1_272' title='bbox 364 512 410 540; x_wconf 96'>Mary</span>
      <span class='ocrx_word' id='word_1_273' title='bbox 524 520 581 535; x_wconf 52'>(19</span>
      <span class='ocrx_word' id='word_1_274' title='bbox 594 520 603 532; x_wconf 67'>F</span>
      <span class='ocrx_word' id='word_1_275' title='bbox 623 520 631 532; x_wconf 69'>8</span>
      <span class='ocrx_word' id='word_1_276' title='bbox 650 520 678 532; x_wconf 37'>Mil</span>
      <span class='ocrx_word' id='word_1_277' title='bbox 745 521 763 534; x_wconf 24'>No)</span>
      <span class='ocrx_word' id='word_1_278' title='bbox 793 520 821 532; x_wconf 81'>Wil</span>
      <span class='ocrx_word' id='word_1_279' title='bbox 887 520 905 533; x_wconf 64'>No</span>
      <span class='ocrx_word' id='word_1_280' title='bbox 935 520 1001 532; x_wconf 89'>Britain</span>
      <span class='ocrx_word' id='word_1_281' title='bbox 1021 520 1094 533; x_wconf 89'>Scottish</span>
      <span class='ocrx_word' id='word_1_282' title='bbox 1115 521 1191 533; x_wconf 24'>Bootland</span>
      <span class='ocrx_word' id='word_1_283' title='bbox 1209 521 1274 536; x_wconf 80'>Glaegow</span>
      <span class='ocrx_word' id='word_1_284' title='bbox 1300 512 1317 534; x_wconf 88'>|v</span>
      <span class='ocrx_word' id='word_1_285' title='bbox 1332 519 1378 530; x_wconf 84'>14679</span>
      <span class='ocrx_word' id='word_1_286' title='bbox 1407 519 1473 534; x_wconf 84'>Glasgow</span>
      <span class='ocrx_word' id='word_1_287' title='bbox 1546 517 1614 534; x_wconf 0'>\25/4/29</span>
      <span class='ocrx_word' id='word_1_288' title='bbox 1664 518 1674 526; x_wconf 86'>~</span>
      <span class='ocrx_word' id='word_1_289' title='bbox 1682 518 1758 532; x_wconf 96'>Scotland</span>
      <span class='ocrx_word' id='word_1_290' title='bbox 1767 520 1832 534; x_wconf 96'>Glasgow</span>
      <span class='ocrx_word' id='word_1_291' title='bbox 1899 524 1907 536; x_wconf 58'>oO</span>
     </span>
     <span class='ocr_line' id='line_1_46' title="bbox 72 537 1675 567; baseline 0.002 -13; x_size 19; x_descenders 4; x_ascenders 4">
      <span class='ocrx_word' id='word_1_292' title='bbox 72 555 77 557; x_wconf 0'>.</span>
      <span class='ocrx_word' id='word_1_293' title='bbox 124 547 137 559; x_wconf 32'>og</span>
      <span class='ocrx_word' id='word_1_294' title='bbox 172 550 177 557; x_wconf 54'>A</span>
      <span class='ocrx_word' id='word_1_295' title='bbox 1008 551 1023 563; x_wconf 45'>A</span>
      <span class='ocrx_word' id='word_1_296' title='bbox 1109 537 1117 567; x_wconf 45'>4‘</span>
      <span class='ocrx_word' id='word_1_297' title='bbox 1300 548 1301 556; x_wconf 78'>|</span>
      <span class='ocrx_word' id='word_1_298' title='bbox 1414 542 1437 557; x_wconf 57'>ke,</span>
      <span class='ocrx_word' id='word_1_299' title='bbox 1453 544 1473 557; x_wconf 38'>37</span>
      <span class='ocrx_word' id='word_1_300' title='bbox 1668 554 1675 560; x_wconf 59'>a</span>
     </span>
     <span class='ocr_line' id='line_1_47' title="bbox 72 547 1852 578; baseline 0.002 -11; x_size 19.274214; x_descenders 3; x_ascenders 5.2742133">
      <span class='ocrx_word' id='word_1_301' title='bbox 72 558 78 567; x_wconf 39'>5</span>
      <span class='ocrx_word' id='word_1_302' title='bbox 91 555 93 568; x_wconf 39'>|</span>
      <span class='ocrx_word' id='word_1_303' title='bbox 118 558 157 572; x_wconf 44'>he</span>
      <span class='ocrx_word' id='word_1_304' title='bbox 164 557 243 571; x_wconf 49'>“Geddes</span>
      <span class='ocrx_word' id='word_1_305' title='bbox 344 551 366 574; x_wconf 68'>3°</span>
      <span class='ocrx_word' id='word_1_306' title='bbox 371 547 429 578; x_wconf 49'>ceorge</span>
      <span class='ocrx_word' id='word_1_307' title='bbox 524 548 555 576; x_wconf 54'>725</span>
      <span class='ocrx_word' id='word_1_308' title='bbox 586 557 632 577; x_wconf 0'>(U/8</span>
      <span class='ocrx_word' id='word_1_309' title='bbox 645 553 773 570; x_wconf 20'>Plastere#’</span>
      <span class='ocrx_word' id='word_1_310' title='bbox 742 549 780 581; x_wconf 94'>Yea</span>
      <span class='ocrx_word' id='word_1_311' title='bbox 793 557 860 572; x_wconf 80'>English</span>
      <span class='ocrx_word' id='word_1_312' title='bbox 888 558 915 570; x_wconf 61'>Yea</span>
      <span class='ocrx_word' id='word_1_313' title='bbox 935 557 1000 570; x_wconf 0'>Britain</span>
      <span class='ocrx_word' id='word_1_314' title='bbox 1022 557 1095 570; x_wconf 0'>“Scottish</span>
      <span class='ocrx_word' id='word_1_315' title='bbox 1115 558 1190 571; x_wconf 15'>@ootlend</span>
      <span class='ocrx_word' id='word_1_316' title='bbox 1208 559 1316 571; x_wconf 48'>Peterhead’,</span>
      <span class='ocrx_word' id='word_1_317' title='bbox 1332 559 1379 571; x_wconf 85'>23588</span>
      <span class='ocrx_word' id='word_1_318' title='bbox 1408 559 1475 574; x_wconf 82'>Glasgow</span>
      <span class='ocrx_word' id='word_1_319' title='bbox 1559 557 1615 573; x_wconf 92'>2/7/29</span>
      <span class='ocrx_word' id='word_1_320' title='bbox 1682 559 1758 571; x_wconf 96'>Scotland</span>
      <span class='ocrx_word' id='word_1_321' title='bbox 1767 559 1852 571; x_wconf 79'>Peterhead</span>
     </span>
     <span class='ocr_line' id='line_1_48' title="bbox 91 571 1671 606; baseline 0.006 -24; x_size 22.274214; x_descenders 6; x_ascenders 5.2742133">
      <span class='ocrx_word' id='word_1_322' title='bbox 91 578 177 594; x_wconf 25'>‘ar</span>
      <span class='ocrx_word' id='word_1_323' title='bbox 543 577 558 590; x_wconf 32'>we</span>
      <span class='ocrx_word' id='word_1_324' title='bbox 587 588 588 592; x_wconf 39'>|</span>
      <span class='ocrx_word' id='word_1_325' title='bbox 650 572 716 602; x_wconf 95'>Textile</span>
      <span class='ocrx_word' id='word_1_326' title='bbox 880 590 881 593; x_wconf 94'>|</span>
      <span class='ocrx_word' id='word_1_327' title='bbox 1300 580 1301 591; x_wconf 95'>|</span>
      <span class='ocrx_word' id='word_1_328' title='bbox 1414 582 1470 606; x_wconf 22'>Seach</span>
      <span class='ocrx_word' id='word_1_329' title='bbox 1532 571 1549 601; x_wconf 0'>Vv.</span>
      <span class='ocrx_word' id='word_1_330' title='bbox 1668 593 1671 598; x_wconf 23'>.</span>
     </span>
     <span class='ocr_line' id='line_1_49' title="bbox 71 581 1917 627; baseline 0.001 -23; x_size 17; x_descenders 3; x_ascenders 3">
      <span class='ocrx_word' id='word_1_331' title='bbox 71 593 78 604; x_wconf 96'>6</span>
      <span class='ocrx_word' id='word_1_332' title='bbox 119 592 165 608; x_wconf 7'>Ao4/</span>
      <span class='ocrx_word' id='word_1_333' title='bbox 184 596 255 608; x_wconf 71'>Kinnear</span>
      <span class='ocrx_word' id='word_1_334' title='bbox 347 581 356 615; x_wconf 1'>eo</span>
      <span class='ocrx_word' id='word_1_335' title='bbox 373 596 449 611; x_wconf 96'>Margaret</span>
      <span class='ocrx_word' id='word_1_336' title='bbox 460 597 499 609; x_wconf 35'>Reid</span>
      <span class='ocrx_word' id='word_1_337' title='bbox 519 597 527 606; x_wconf 89'>v</span>
      <span class='ocrx_word' id='word_1_338' title='bbox 538 594 555 607; x_wconf 65'>NV</span>
      <span class='ocrx_word' id='word_1_339' title='bbox 585 595 603 627; x_wconf 0'>‘c</span>
      <span class='ocrx_word' id='word_1_340' title='bbox 612 590 632 608; x_wconf 92'>Vg</span>
      <span class='ocrx_word' id='word_1_341' title='bbox 645 591 773 609; x_wconf 32'>Dperator’“Yea</span>
      <span class='ocrx_word' id='word_1_342' title='bbox 793 593 859 608; x_wconf 96'>English</span>
      <span class='ocrx_word' id='word_1_343' title='bbox 888 594 915 606; x_wconf 60'>Yea</span>
      <span class='ocrx_word' id='word_1_344' title='bbox 935 593 1001 606; x_wconf 90'>Britain</span>
      <span class='ocrx_word' id='word_1_345' title='bbox 1015 590 1095 606; x_wconf 88'>‘Scottish</span>
      <span class='ocrx_word' id='word_1_346' title='bbox 1116 594 1190 607; x_wconf 58'>Scotland</span>
      <span class='ocrx_word' id='word_1_347' title='bbox 1210 595 1265 607; x_wconf 74'>Dundee</span>
      <span class='ocrx_word' id='word_1_348' title='bbox 1300 596 1325 608; x_wconf 16'>|</span>
      <span class='ocrx_word' id='word_1_349' title='bbox 1342 594 1378 606; x_wconf 78'>9088</span>
      <span class='ocrx_word' id='word_1_350' title='bbox 1408 594 1474 609; x_wconf 92'>Glasgow</span>
      <span class='ocrx_word' id='word_1_351' title='bbox 1550 592 1615 609; x_wconf 80'>10/4/29</span>
      <span class='ocrx_word' id='word_1_352' title='bbox 1683 594 1758 607; x_wconf 96'>Scotland</span>
      <span class='ocrx_word' id='word_1_353' title='bbox 1767 594 1823 606; x_wconf 96'>Dundee</span>
      <span class='ocrx_word' id='word_1_354' title='bbox 1895 607 1917 623; x_wconf 60'>5</span>
     </span>
     <span class='ocr_line' id='line_1_50' title="bbox 1452 616 1470 628; baseline 0 -9; x_size 23.628012; x_descenders 5.5; x_ascenders 5.875">
      <span class='ocrx_word' id='word_1_355' title='bbox 1452 616 1470 628; x_wconf 26'>ae</span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_30' title="bbox 1408 612 1440 648">
    <p class='ocr_par' id='par_1_30' lang='eng' title="bbox 1408 612 1440 648">
     <span class='ocr_line' id='line_1_51' title="bbox 1408 612 1440 648; baseline 0 0; x_size 49.333332; x_descenders 12.333333; x_ascenders 12.333333">
      <span class='ocrx_word' id='word_1_356' title='bbox 1408 612 1440 648; x_wconf 95'> </span>
     </span>
    </p>
   </div>
   <div class='ocr_carea' id='block_1_31' title="bbox 71 614 1842 648">
    <p class='ocr_par' id='par_1_31' lang='eng' title="bbox 71 614 1842 648">
     <span class='ocr_line' id='line_1_52' title="bbox 71 614 1842 648; baseline 0.002 -7; x_size 20; x_descenders 3; x_ascenders 5">
      <span class='ocrx_word' id='word_1_357' title='bbox 71 630 78 642; x_wconf 43'>7)</span>
      <span class='ocrx_word' id='word_1_358' title='bbox 118 625 155 647; x_wconf 92'>Ze</span>
      <span class='ocrx_word' id='word_1_359' title='bbox 183 631 244 643; x_wconf 43'>|Miller</span>
      <span class='ocrx_word' id='word_1_360' title='bbox 342 624 369 648; x_wconf 45'>oY</span>
      <span class='ocrx_word' id='word_1_361' title='bbox 374 632 420 643; x_wconf 92'>Sarah</span>
      <span class='ocrx_word' id='word_1_362' title='bbox 432 632 479 647; x_wconf 92'>Logan</span>
      <span class='ocrx_word' id='word_1_363' title='bbox 513 620 555 648; x_wconf 27'>Ve4</span>
      <span class='ocrx_word' id='word_1_364' title='bbox 571 615 632 644; x_wconf 56'>drs</span>
      <span class='ocrx_word' id='word_1_365' title='bbox 644 626 699 644; x_wconf 74'>4lerk</span>
      <span class='ocrx_word' id='word_1_366' title='bbox 736 631 773 644; x_wconf 40'>‘Yes</span>
      <span class='ocrx_word' id='word_1_367' title='bbox 793 632 858 647; x_wconf 92'>English</span>
      <span class='ocrx_word' id='word_1_368' title='bbox 880 626 927 645; x_wconf 40'>Yee</span>
      <span class='ocrx_word' id='word_1_369' title='bbox 929 620 1001 648; x_wconf 40'>Britain</span>
      <span class='ocrx_word' id='word_1_370' title='bbox 1015 632 1095 645; x_wconf 67'>‘Scottish</span>
      <span class='ocrx_word' id='word_1_371' title='bbox 1113 629 1191 646; x_wconf 6'>@otland</span>
      <span class='ocrx_word' id='word_1_372' title='bbox 1209 633 1285 645; x_wconf 80'>Greenock</span>
      <span class='ocrx_word' id='word_1_373' title='bbox 1300 624 1379 644; x_wconf 39'>|m~15175</span>
      <span class='ocrx_word' id='word_1_374' title='bbox 1408 627 1473 648; x_wconf 54'>Glasgow</span>
      <span class='ocrx_word' id='word_1_375' title='bbox 1547 627 1616 648; x_wconf 59'>45/4/29</span>
      <span class='ocrx_word' id='word_1_376' title='bbox 1686 614 1758 648; x_wconf 0'>ootaand</span>
      <span class='ocrx_word' id='word_1_377' title='bbox 1767 633 1842 645; x_wconf 96'>Greenock</span>
     </span>
    </p>
   </div>
  </div>
 </body>
</html>

```
</details>