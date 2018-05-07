# freetype

This is a clone repo from golang/freetype with some special changes.

1. search cmap subtables in below order so that to ensure always get characters as many as possible

platformID | platformSpecificID | Description
-----------|--------------------|--------
0 |	4 |	Unicode, 2.0 or later.
0 |	< 4 |	Unicode, version of Unicode
3 |	10 |	Windows, Unicode UCS-4
3 |	1 |	Windows, Unicode BMP (UCS-2)
3 |	0 |	Windows, Symbol
    