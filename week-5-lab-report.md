# Week 5 Lab Report

## grep -c
This command returns the number of lines in the chosen file that contain the given string. This could be useful in the way that Ctrl-f takes a specific phrase you are looking for and shows you all of its instances in a document.  

Example 1:
```
[cs15lfa22ab@ieng6-203]:docsearch:171$ grep -c "mechanism" technical/biomed/1468-6708-3-7.txt
9
```
This returns the number of times "mechanism" appears in the given file.

Example 2:
```
[cs15lfa22ab@ieng6-203]:docsearch:181$ grep -c "important" technical/plos/journal.pbio.002001*.txt
technical/plos/journal.pbio.0020010.txt:2
technical/plos/journal.pbio.0020012.txt:0
technical/plos/journal.pbio.0020013.txt:1
technical/plos/journal.pbio.0020019.txt:2
```
This returns the number of times "important" appears in each of the given files.

Example 3:
```
[cs15lfa22ab@ieng6-203]:docsearch:186$ grep -c "religion" technical/911report/chapter-13.*.txt
technical/911report/chapter-13.1.txt:0
technical/911report/chapter-13.2.txt:0
technical/911report/chapter-13.3.txt:0
technical/911report/chapter-13.4.txt:0
technical/911report/chapter-13.5.txt:5
```
This returns the number of times "religion" appears in the 911report/chapter-13 files, for each file.

## grep -n
This command prints out all the lines in the file that contain the matching string with their line numbers before it. If you want to see where a specific word or phrase occurs in a file, you can use this command to see what line numbers it occurs at and then just navigate to those lines.

Example 1:
```
[cs15lfa22ab@ieng6-203]:docsearch:172$ grep -n "mechanism" technical/biomed/1468-6708-3-7.txt
14:        obvious suggestion of a mechanism by which peripheral
34:        mechanisms leading to an inferior performance in
165:          direct myocardial damage through many mechanisms, which
182:          Other mechanisms for cellular injury have been
184:          antagonists alter cellular repair mechanisms, possibly
267:        The literature suggests several mechanisms by which
273:        disease. If this is the mechanism responsible for
294:        the mechanism for reduced protection compared to diuretics
302:        Whatever mechanisms were responsible for the heart
```
This returns the line numbers and lines "mechanism" appears in for the given file.

Example 2:
```
[cs15lfa22ab@ieng6-203]:docsearch:182$ grep -n "death" technical/911report/*.txt
technical/911report/chapter-10.txt:60:                them." He quoted Psalm 23-"though I walk through the valley of the shadow of death .
technical/911report/chapter-12.txt:621:                    nothing to offer their children but visions of violence and death. America and
technical/911report/chapter-12.txt:626:            That vision of the future should stress life over death: individual educational and
technical/911report/chapter-12.txt:874:                    worked. The death or capture of several important facilitators has decreased the
technical/911report/chapter-13.4.txt:65:                The latter explosion caused the death of a passenger and extensive damage to the
technical/911report/chapter-13.4.txt:302:                Intelligence report, interrogation of KSM, Jan. 9, 2004. For Atef 's death, see DOS
technical/911report/chapter-13.5.txt:1441:                protocol and prescripted announcements and the death of the director of fire safety
technical/911report/chapter-13.5.txt:2073:            188. According to the number of death certificates issued by the New York City
technical/911report/chapter-13.5.txt:2081:                these first responder death totals were the largest in U.S. history is based on our
technical/911report/chapter-13.5.txt:2108:            192. For the death toll, see FBI report, list of Pentagon victims, undated. For
technical/911report/chapter-13.5.txt:2136:                2004. For the updated death certificate information, see New York City report,"WTC
technical/911report/chapter-13.5.txt:2702:                Apr. 8-9, 2004; Apr. 28, 2004); Tommy Franks interview (Apr. 9, 2004). On death of
technical/911report/chapter-2.txt:87:                Soon after the Prophet's death, the question of choosing a new leader, or caliph,
technical/911report/chapter-2.txt:176:                Islamic nation, a nation that al Qaeda's leaders said "desires death more than you
technical/911report/chapter-2.txt:938:                Americans. Interviewed later about the deaths of the Africans, Bin Ladin answered
technical/911report/chapter-3.txt:162:                in the 1970s. Two years after Hoover's death in 1972, congresCOUNTERTERRORISM
technical/911report/chapter-3.txt:2030:            Even after the embassy attacks, Bin Ladin had been responsible for the deaths of
technical/911report/chapter-3.txt:2213:                camps hit by U.S. missiles, leading to the death of Pakistanis.
technical/911report/chapter-3.txt:3105:                Ladin's death.
technical/911report/chapter-6.txt:77:                accomplices were sentenced to death. In custody, Hijazi's younger brother said that
technical/911report/chapter-7.txt:1541:                death would also appease the Taliban when the 9/11 attacks happened. There are also
technical/911report/chapter-9.txt:223:                three-year period since accurate measurements began in 1946. Firefighter deaths-a
technical/911report/chapter-9.txt:1606:                been a much higher death total. It is impossible to measure how many more civilians
```
This returns the file name, line number, and line for each file in 911report files where "death" appears.

Example 3:
```
[cs15lfa22ab@ieng6-203]:docsearch:188$ grep -n "unfathomable" technical/plos/*.txt
[cs15lfa22ab@ieng6-203]:docsearch:190$ grep -n "unfathomable" technical/*/*.txt
technical/911report/chapter-9.txt:1392:                found the full collapse of the South Tower so unfathomable that they radioed back to
```
This returns the file name, line number, and line for each of the selected files where "unfathomable" appears. There was none for the first one.

## grep -l
This command returns only the file names of all the chosen files which contain the given string. This could be useful when sifting through many files of data and you want to create a list of only the ones that talk about a certain topic or have a specific key term in them.

Example 1:
```
[cs15lfa22ab@ieng6-203]:docsearch:175$ grep -l "mechanism" technical/biomed/ar*.txt
technical/biomed/ar104.txt
technical/biomed/ar118.txt
technical/biomed/ar140.txt
technical/biomed/ar297.txt
technical/biomed/ar309.txt
technical/biomed/ar321.txt
technical/biomed/ar331.txt
technical/biomed/ar383.txt
technical/biomed/ar387.txt
technical/biomed/ar408.txt
technical/biomed/ar429.txt
technical/biomed/ar430.txt
technical/biomed/ar601.txt
technical/biomed/ar612.txt
technical/biomed/ar615.txt
technical/biomed/ar619.txt
technical/biomed/ar624.txt
technical/biomed/ar745.txt
technical/biomed/ar79.txt
technical/biomed/ar792.txt
technical/biomed/ar795.txt
technical/biomed/ar93.txt
```
This returns the file names of the biomed files (beginning with "ar") that have the word "mechanism".

Example 2:
```
[cs15lfa22ab@ieng6-203]:docsearch:184$ grep -l "determine" technical/government/Alcohol_Problems/Session2-PDF.txt
technical/government/Alcohol_Problems/Session2-PDF.txt
```
This returns the file names of the selected files in Alcohol_Problems that have the word "determine".

Example 3:
```
[cs15lfa22ab@ieng6-203]:docsearch:192$ grep -l "antimicrobial" technical/*/*0*.txt
technical/biomed/1471-2180-1-26.txt
technical/biomed/1472-6750-2-2.txt
technical/biomed/1476-0711-2-3.txt
technical/biomed/1476-0711-2-7.txt
technical/biomed/gb-2003-4-3-r20.txt
technical/plos/journal.pbio.0020012.txt
technical/plos/journal.pbio.0020276.txt
technical/plos/journal.pbio.0020307.txt
```
This returns the file names of the selected files that have the word "antimicrobial".