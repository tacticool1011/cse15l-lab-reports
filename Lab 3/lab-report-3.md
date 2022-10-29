# Lab Report 3 - Commands

## ``grep`` Command

### ``-c`` Displays the count of number of matches
- ``-c`` is useful when you just want to look at numbers and not the contents of the matches.

```
Input:
grep -c "the" ./911report/chapter-1.txt

Ouput:
313
```

- It searches the contents of chapter-1.txt and sees how many words match with "the".
- The output is printed as the total unmber of matches.


```
Input:
grep -c "nation" ./911report/*

Ouput:
./911report/chapter-1.txt:22
./911report/chapter-10.txt:30
./911report/chapter-11.txt:33
./911report/chapter-12.txt:77
./911report/chapter-13.1.txt:84
./911report/chapter-13.2.txt:16
./911report/chapter-13.3.txt:33
./911report/chapter-13.4.txt:22
./911report/chapter-13.5.txt:51
./911report/chapter-2.txt:23
./911report/chapter-3.txt:89
./911report/chapter-5.txt:20
./911report/chapter-6.txt:37
./911report/chapter-7.txt:17
./911report/chapter-8.txt:12
./911report/chapter-9.txt:19
./911report/preface.txt:8
```

- It searches the contents of all the files in the directory ``./911report/`` that contains the word ``nation``.
- The output prints out every single file in that directory and indicates how many matches it find for each file.

```
Input:
grep -c "counter" ./government/Alcohol_Problems/*

Ouput:
./government/Alcohol_Problems/DraftRecom-PDF.txt:0
./government/Alcohol_Problems/Session2-PDF.txt:1
./government/Alcohol_Problems/Session3-PDF.txt:4
./government/Alcohol_Problems/Session4-PDF.txt:3
```

- It searches the contents of all the files in the ``./government/Alcohol_Problems/`` directory that contains the word ``counter``.
- The output searches the contents of each file whether or not there is a match or not.
- If there is no match, it will print out 0 for that file path.

### ``-l`` Displays the file names that matches the pattern
- ``l`` is useful when you just want to see which files contain the matches.

```
Input:
grep -l "defense" ./911report/*

Ouput:
./911report/chapter-1.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
./911report/chapter-12.txt
./911report/chapter-13.1.txt
./911report/chapter-13.3.txt
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-2.txt
./911report/chapter-3.txt
./911report/chapter-6.txt
./911report/chapter-8.txt
./911report/chapter-9.txt
```

- It searches the contents of all the files in the directory ``./911report/`` that contains the word ``defense``.
- Instead of indicating how many matches for each file, it just prints the files that contain matches.

```
Input:
grep -l "patient" ./government/*/*

Ouput:
./government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
./government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
./government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
./government/Alcohol_Problems/DraftRecom-PDF.txt
./government/Alcohol_Problems/Session2-PDF.txt
./government/Alcohol_Problems/Session3-PDF.txt
./government/Alcohol_Problems/Session4-PDF.txt
./government/Gen_Account_Office/Oct15-1999_gg00026t.txt
./government/Gen_Account_Office/Sept27-2002_d02966.txt
./government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./government/Gen_Account_Office/Testimony_cg00010t.txt
./government/Gen_Account_Office/d01591sp.txt
./government/Gen_Account_Office/d0269g.txt
./government/Gen_Account_Office/d03419sp.txt
./government/Gen_Account_Office/gg96118.txt
./government/Gen_Account_Office/og96041.txt
./government/Gen_Account_Office/og98030.txt
./government/Gen_Account_Office/og98041.txt
./government/Media/Politician_Practices.txt
./government/Media/Understanding.txt
./government/Media/highlight_Senior_Day.txt
```

- It searches the contents of all the files in the directory ``./government/*/*`` that contains the word ``patient``.
- The output contains all the file directories that contains a match.

```
Input:
grep -l "bomb" ./government/Alcohol_Problems/Session2-PDF.txt

Ouput:

```

- It searches the contents of in the file ``./government/Alcohol_Problems/Session2-PDF.txt`` that contains the word ``bomb``.
- Since there were no matches, it printed nothing in the output.

### ``-w`` Checking for the whole words in a file
- ``w`` is useful when you want to see which files have matches and where the matches are in the content.

```
Input:
grep -w "civilization" ./911report/*

Ouput:
./911report/chapter-10.txt:                States." This is civilization's fight," he said. "We ask every nation to join
./911report/chapter-12.txt:                itself caught up in a clash within a civilization. That clash arises from particular
./911report/chapter-2.txt:                saddening to tell you that you are the worst civilization witnessed by the history
```

- It searches the contents of all the files in the directory ``./911report/*`` that contains the word ``civilization``.
- In the output, it prints the matching directories as well as the contents of the file that matches the word.

```
Input:
grep -w "a;slkdfja;slkjdfd" ./*/*/*

Ouput:

```

- It searches the contents of all the files in the directory ``./*/*/*`` that contains the word ``a;slkdfja;slkjdfd``.
- Since there were no matches, it printed nothing.

```
Input:
grep -w "yes" ./government/Alcohol_Problems/Session2-PDF.txt

Ouput:
a screen for alcohol abuse and dependence, has 24 yes/no questions.
has 35 yes/no questions. While lengthy, the SAAST has the advantage
improve efficiency.35 If one question answered "yes" yields a
```

- It searches the contents of in the file ``./government/Alcohol_Problems/Session2-PDF.txt`` that contains the word ``yes``.
- Since there were matches and it's a singular file, it printed out only the matching contents.


