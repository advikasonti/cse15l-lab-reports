# Lab Report 3

##  Researching Commands (find)

### Option 1: -name

#### Example 1
The `-name` command searches for files with the given string in the name and returns a full list of them. In the code block below, I searched for files that begin with the word `History` in the title, and it returned a list of all of the files in `written_2` that contained that in the name.
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

#### Example 1
The `-type` command intuitively searched for a file or directory of certain type. Below, I used it to find `d`, which looks for anything that is of a directory type under `written_2`. 
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














