# Lab Report 3

##  Researching Commands (find)

### Option 1: -name
The `-name` command searches for files with the given string in the name and returns a full list of them. 

#### Example 1
In the code block below, I searched for files that begin with the word `History` in the title, and it returned a list of all of the files in `written_2` that contained that in the name.
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2 -name "History*" 
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/HistoryJamaica.txt
written_2/travel_guides/berlitz1/HistoryEgypt.txt
written_2/travel_guides/berlitz1/HistoryIsrael.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/HistoryDublin.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryMallorca.txt
written_2/travel_guides/berlitz1/HistoryJerusalem.txt
written_2/travel_guides/berlitz1/HistoryMadrid.txt
written_2/travel_guides/berlitz1/HistoryHongKong.txt
written_2/travel_guides/berlitz1/HistoryIstanbul.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt
written_2/travel_guides/berlitz1/HistoryGreek.txt
written_2/travel_guides/berlitz1/HistoryHawaii.txt
written_2/travel_guides/berlitz1/HistoryMadeira.txt
written_2/travel_guides/berlitz1/HistoryMalaysia.txt
written_2/travel_guides/berlitz1/HistoryIbiza.txt
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
written_2/travel_guides/berlitz1/HistoryFWI.txt
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
```
#### Example 2
In the example below, I searched specifically in the `non-fiction` directory under `written_2` for all of the files that included `ch2` in the name.
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2/non-fiction -name "*ch2*"
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
```

### Option 2: -type
The `-type` command intuitively searched for a file or directory of certain type. 

#### Example 1
Below, I used it to find `d`, which looks for anything that is of a directory type under `written_2`. 
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2/non-fiction -name "*ch2*"
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
```
#### Example 2
With the knowledge from the above example, I then went more specifically into the `non-fiction/OUP/Castro` directory under `written_2` to find everything of type file, or `f`, in that specified directory.
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2/non-fiction/OUP/Castro -type f
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chP.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chM.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chO.txt
```

### Option 3: -size
The `-size` command searched for files with a specified size given by any of the following values: `c`: bytes, `k`: kilobytes, `M`: megabytes, `G`: gigabytes. You can also specify the search to find files that are larger or smaller than the given size using `+` or `-` before the value to be searched for.

#### Example 1
In the example below, I found files in the `non-fiction/OUP` directory under `written_2` that are smaller than 40 kilobytes.
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2/non-fiction/OUP -size -40k
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/.DS_Store
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Rybczynski
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Kauffman/ch5.txt
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Castro
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chO.txt
```
#### Example 2
In the code block below, I used a similar search while slightly altering the arguments to find all the files under `non-fiction/OUP` that are larger than 70 kilobytes.
```
advikasonti@Advikas-MacBook-Pro docsearch % find written_2/non-fiction/OUP -size +70k
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Kauffman/ch3.txt
written_2/non-fiction/OUP/Kauffman/ch4.txt
written_2/non-fiction/OUP/Kauffman/ch8.txt
written_2/non-fiction/OUP/Kauffman/ch9.txt
```















