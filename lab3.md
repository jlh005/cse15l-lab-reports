<h1> Lab Report 3 </h1>

For this lab report, I will be doing a report on the grep command, which is a command to help find a specific pattern or text in a file.
The grep command has numerous options that can help perfect the use of the grep command.

<h2> -r option </h2>

This option allows the grep command to search recursively through a directory and its following subdirectories to find a certain word.
Here are some examples of this command at work.

```
grep -r "among us" ./technical

```
Once run, this command gives the following output in the terminal.

```
$ grep -r "among us" ./technical
./technical/biomed/1471-2261-3-5.txt:        clinically diagnosed valve disease among users of
./technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt:unreasonable discrimination among users of the mails, nor shall it

```

You can see that grep here went through all the subdirectories of technical into biomed and government to find all instances of lines
that contained "among us". The -r option is very useful if you want to search for a specific text in a large directory or subdirectory.

Here's another example.

```
grep -r "gracious manner" ./technical

```
Here, grep found no lines that contained the words, "gracious manner" in all of the technical directory. In this case there would just be a blank output and you would only see
the command you inputted. The -r command is also useful if you just want to check for a word in a directory and are too lazy to type out the file names you want to search.

```
$ grep -r "gracious manner" ./technical

```

<h2> -i option </h2>

This option allows the grep command to perform a case insensitive search.

Here's an example of this at work.

```
grep -i "lowering" ./technical/biomed/1468-6708-3-3.txt

```

The output when run,

```
$ grep -i "lowering" ./technical/biomed/1468-6708-3-3.txt
        these trials did not assess the effect of lipid-lowering
        lipid-lowering therapy would provide incremental benefit if
        Ischemia Reduction with Aggressive Cholesterol Lowering
        for a number of reasons. Although lipid-lowering therapy
        studies suggest that lipid-lowering agents exert short-term
        could still make a compelling argument that lipid-lowering
        in-hospital initiation of lipid-lowering therapy appears to
        non-pharmacologic lipid-lowering interventions to attain
        lipid-lowering therapy from patients who present with an
        and to date our efforts at cholesterol lowering in the
        aggressive vs. earlier lipid lowering therapy.
        less aggressive lipid-lowering in
        Lowering; LDL = low density lipoprotein; RR = relative
```

You can see that grep found cases of both "lowering" and "Lowering" ignoring the case sensitive "lowering" we put in our command because of the -i option.
The -i command is particularly useful if you aren't exactly sure what case the text you're looking for is.

Here is another example.

```
grep -i "however" ./technical/plos/journal.pbio.0020001.txt

```

And the output,

```
$ grep -i "however" ./technical/plos/journal.pbio.0020001.txt
        The total number of publications, however, is not necessarily the best measure for
        important question, however, is why the number of publications per dollar invested in
        however, Latin America represented only 6%, while Canada and United States accounted,
        However, publishing in
        activities, however, requires a greater proportion of research money being spent on
```

Again, you can see that grep finds both uppercase "However" and "however" in its output in the file. The -i command is also useful
for if you want to find both cases of a text and don't want it to omit a specific case.

<h2> -v option </h2>

This option makes grep do the opposite of what it's supposed to do and instead excludes the lines that matches the text.

For an example, let's try the -v command on a previous file we've already searched.

```
grep -v "however" ./technical/plos/journal.pbio.0020001.txt

```

Due to the nature of the option, I will not be posting the full output because of how large it is. What I will show is an interesting excerpt from the output.

```
 Science and
        Nature , Latin America had 7% of the publications within the Americas
        versus 6% in the top 20 ecological journals, whereas the United States and Canada had 81%
        versus 82% and 12% versus 13%, respectively. These similarities suggest that the Latin
        American researchers are not shying away from the two top-ranked general science journals.
        However, publishing in
        Science and
```

Note that the command only excludes the text "however"  and not "However". The -v command excludes the text, case sensitive only. The -v command is useful when you want to exclude
certain patterns in your search.

Another example:

```
grep -v "i" ./technical/biomed/1468-6708-3-3.txt

```

And the output,

```
$ grep -v "i" ./technical/biomed/1468-6708-3-3.txt




        The problem
        recently


        The answer?
        fatal or non-fatal stroke by 0.8% (0.8% vs. 1.6%; RR 0.50,
        weeks, the adjusted mean LDL cholesterol decreased to 72


        The MIRACuLous


        The not so MIRACuLous
        early after coronary


        recommended cholesterol targets [ 23 24 25 ] ; newer
        acute coronary syndrome would be to accept the status quo,
        .


        More MIRACLes ahead?
        an acute coronary syndrome (ACS) at one year. If A-2-Z
        these agents early after an acute coronary syndrome. If
        more vs.


        Merck.


        HMG CoA = 3-Hydroxy-3-methylgluatryl coenzyme A; MIRACL

```

Here, the command completely excluded every instance of "i" that it could find in each line, drastically cutting down the text of the file. If you think about it, the -v option is quite useful for 
cutting down the size of files.

<h2> -c option </h2>

This option tells the grep command to only count the number of lines that contain the word.

Here's an example.
