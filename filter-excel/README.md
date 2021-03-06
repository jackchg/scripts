# Description
A Python script that takes an Excel spreadsheet with a single sheet of
information and prints all rows containing user-chosen keywords in a
specific column.

# How to Use
python filter\_excel.py [-k keyword\_file\_name]
                        [-s sheet\_file\_name]
                        [-r result\_file\_name]
                        [\-\-case-insensitive]
                        num\_rows
                        col\_num

The "-k" flag is optional. If not passed, then the program expects a default
keywords file named "keywords.txt" in the current directory.

The "-s" flag is optional. If not passed, then the program expects a default
Excel sheet file named "sheet.xlsx" in the current directory.

The "-r" flag is optional. If not passed, then the program creates or
overwrites a text file called "results.txt" into the current directory.

The "--case-insensitive" flag is optional. If passed, then all searches for
keywords are case insensitive. For example, if passed, the keywords "SEA" and
"sea" will be equivalent.

num\_rows: The number of rows of data.

col\_num: The column number to find keywords in. (A=1, B=2, C=3,..., Z=26)

# "keywords.txt" Requirements
Please put each keyword on a new line and surrounded by quotation marks. The
quotation marks allow you to add leading spaces for a keyword.

Example "keywords.txt":  
"apple"  
"banana "  
" coconut"  
" durian "  

As you can see, surrounding quotes allow you to distinct word fragments
or smaller words from whole or larger words. For example, distinguishing
"sea" from "research" can be done by using the keyword " sea ". Note,
however, that you will not find phrases like "sea." or "sea," as a result.

Keywords are case sensitive. There is no support for wildcard characters.
