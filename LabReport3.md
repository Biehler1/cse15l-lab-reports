# Lab 3
## Part 1
Bug: The bug that we are going to examine is the reversed() method from the ArrayExamples.java class. The problem seems to be that the original reversed() method would change the inputted array, and assign it blank (0) values from a new array that was created. Therefore, the fix seems to be just to switch the new array with the old array in the code and return the new array.

1. Failure Inducing Input: 
```
  @Test
  public void testReversed3Inputs() {
    int[] input = {1, 2, 3};
    int[] temp = {1, 2, 3};

    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input));

    //Checks that the original array wasn't changed
    assertArrayEquals(temp, input);
  }
```
2. Non-Failure Inducing Input:
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
3. Symptom:
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/45a83193-a815-4fa2-a871-9b73f33ca9cc)
4. Bug fix:

Before:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; ++i) {
      newArray[arr.length-1-i] = arr[i];
    }
    return newArray;
  }
```

Explanation:
Originally, the issue was that the original array (arr) was assigned values from the new array created (newArray that had all 0 values) instead of the other way around. Then, it returned the original array (arr) when it was supposed to return a new array (newArray). To fix this, I flipped the assignment of values from the new array (newArray) to the old array (arr) to the assignment of values from the old array (arr) to the new array (newArray). This was demonstrated through changing the line `arr[i] = newArray[arr.length - i - 1];` to `newArray[arr.length-1-i] = arr[i];`. To make sure the program returned a new array instead of changing a pre-existing one, I also made sure to make the program `return newArray;` instead of `return arr;`. These changes made it so the reversed() method worked properly and that the values of the original array (arr) wasn't changed at all, just like the description of the method.

# Part 2
The command we will be exploring is grep. All of the information gathered about grep comes from [https://www.geeksforgeeks.org/grep-command-in-unixlinux/#](https://www.geeksforgeeks.org/grep-command-in-unixlinux/#).

1. grep -c

Example 1:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -c "planes" ./technical/911report/*.txt
./technical/911report/chapter-1.txt:16
./technical/911report/chapter-10.txt:0
./technical/911report/chapter-11.txt:3
./technical/911report/chapter-12.txt:1
./technical/911report/chapter-13.1.txt:1
./technical/911report/chapter-13.2.txt:5
./technical/911report/chapter-13.3.txt:1
./technical/911report/chapter-13.4.txt:13
./technical/911report/chapter-13.5.txt:6
./technical/911report/chapter-2.txt:0
./technical/911report/chapter-3.txt:2
./technical/911report/chapter-5.txt:30
./technical/911report/chapter-6.txt:2
./technical/911report/chapter-7.txt:20
./technical/911report/chapter-8.txt:2
./technical/911report/chapter-9.txt:3
./technical/911report/preface.txt:0
```

Example 2:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -c "environment" ./technical/government/Env_Prot_Agen/*.txt
./technical/government/Env_Prot_Agen/1-3_meth_901.txt:1
./technical/government/Env_Prot_Agen/atx1-6.txt:2
./technical/government/Env_Prot_Agen/bill.txt:16
./technical/government/Env_Prot_Agen/ctf1-6.txt:2
./technical/government/Env_Prot_Agen/ctf7-10.txt:0
./technical/government/Env_Prot_Agen/ctm4-10.txt:1
./technical/government/Env_Prot_Agen/final.txt:26
./technical/government/Env_Prot_Agen/jeffordslieberm.txt:4
./technical/government/Env_Prot_Agen/multi102902.txt:12
./technical/government/Env_Prot_Agen/nov1.txt:30
./technical/government/Env_Prot_Agen/ro_clear_skies_book.txt:11
./technical/government/Env_Prot_Agen/section-by-section_summary.txt:1
./technical/government/Env_Prot_Agen/tech_adden.txt:29
./technical/government/Env_Prot_Agen/tech_sectiong.txt:4
```

Explanation:
The -c option seems to count the number of words in each file that contain the specific pattern (for example, in example 1, `./technical/911report/chapter-1.txt` would contain 16 instances of "planes", while in example 2, `./technical/government/Env_Prot_Agen/final.txt` would contain 26 instances of "environment"). This would be useful to see how many times a word or piece of code is used within individual files. 

2. grep -l

Example 1:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -l "Saddam" ./technical/911report/*.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-5.txt
```

Example 2:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -l "alcohol" ./technical/government/*/*.txt
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
./technical/government/Gen_Account_Office/og97002.txt
./technical/government/Media/Abuse_penalties.txt
./technical/government/Media/Annual_Fee.txt
./technical/government/Media/Higher_Registration_Fees.txt
./technical/government/Media/Paralegal_Honored.txt
./technical/government/Media/Weak_economy.txt
```

Explanation:
The -l option finds and returns all files that comtain the designated pattern (in this case being "Saddam" for all the txt files in the 911report directory and "alcohol" for all the txt files in the government directory and all of its subdirectories). This is useful when you want to find specific files that mentions a word or has a specific line of code, allowing significantly less manual searching.

3. grep -e

Example 1:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -e "potassium" ./technical/plos/*.txt
./technical/plos/pmed.0020140.txt:          electrolytic abnormalities such as sodium and potassium loss and possibly intravascular
./technical/plos/pmed.0020140.txt:          As a general rule, normal serum potassium levels do not necessarily imply that the
./technical/plos/pmed.0020140.txt:          total body potassium content is normal, as only 2% of total body potassium stores are
./technical/plos/pmed.0020140.txt:          altered and many factors may influence serum potassium levels and total body potassium
./technical/plos/pmed.0020140.txt:          stores. These factors are (a) insulin, which increases potassium uptake by cells; (b)
./technical/plos/pmed.0020140.txt:          potassium for hydrogen ions; and (c) hyperosmolarity, which causes a rearrangement of
./technical/plos/pmed.0020140.txt:          potassium and fluid from intracellular to extracellular compartments. In patients with
./technical/plos/pmed.0020140.txt:          diabetes who have normal renal function and normal serum potassium concentration, 10 to
./technical/plos/pmed.0020140.txt:          20 mEq of potassium should be added to each liter of dextrose-containing fluid. A higher
./technical/plos/pmed.0020140.txt:          dose is required in patients with hypokalemia. If serum potassium levels are greater than
./technical/plos/pmed.0020140.txt:          5.5 mEq/l, potassium therapy should be withheld from the IV fluids and potassium serum
```

Example 2:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -e "sodium bicarbonate" ./technical/biomed/*.txt
./technical/biomed/1471-2121-1-2.txt:          (Colorado Serum Company), 0.22% sodium bicarbonate, 4 mM
./technical/biomed/1471-2180-3-5.txt:          (Sigma), 2 g of sodium bicarbonate per liter, 75 μg of
./technical/biomed/gb-2001-2-4-research0011.txt:        The human sodium bicarbonate cotransporters (NBCs),
./technical/biomed/gb-2001-2-4-research0011.txt:          predict yet another novel sodium bicarbonate
./technical/biomed/gb-2001-2-4-research0011.txt:          domains characteristic of sodium bicarbonate
```

Explanation:
The -e option finds and returns all lines that contain the designated pattern (in this case "potassium" for all of the txt files in the plos directory and "sodium bicarbonate" for all of the txt files in the biomed directory) as well as the files each of the lines were found in. This would be useful to find specific lines that contain words/code and gaining context around how they are used, allowing you to better identify where to search. 

#4. grep -C n (with n being a positive integer)

Example 1:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -C 1 "second tower" ./technical/911report/*.txt
./technical/911report/chapter-1.txt-
./technical/911report/chapter-1.txt:    The President and the Vice President The President was seated in a classroom when, at 9:05, Andrew Card whispered to him: "A second plane hit the second tower. America is under attack." The President told us his instinct was to project calm, not to have the country see an excited reaction at a moment of crisis. The press was standing behind the children; he saw their phones and pagers start to ring. The President felt he should project strength and calm until he could better understand what was happening.
./technical/911report/chapter-1.txt-
--
./technical/911report/chapter-13.2.txt-                file, Identification Technician position, channel 5. At 9:10:22, the Otis fighters
./technical/911report/chapter-13.2.txt:                were told by Boston Center that the second tower had been struck. At 9:12:54, the
./technical/911report/chapter-13.2.txt-                Otis fighters told their Boston Center controller that they needed to establish a
```

Example 2:
```
mfbie@mbiehler MINGW64 ~/.vscode/Coding Projects/CSE 15L/docsearch (main)
$ grep -C 2 "alkaline" ./technical/plos/*.txt
./technical/plos/pmed.0020161.txt-        Osteogenesis was demonstrated by specific staining for calcium deposition in the matrix
./technical/plos/pmed.0020161.txt-        (von Kossa, Figure 2C; or Alizarin Red, Figure S2A) and increased expression of
./technical/plos/pmed.0020161.txt:        bone-specific alkaline phosphatase and
./technical/plos/pmed.0020161.txt-        bone sialoprotein at day 28 of treatment (Figures 2C and S2B). At day 28,
./technical/plos/pmed.0020161.txt-        Alizarin Red staining was detected in approximately 70% of all cells. Throughout these
--
./technical/plos/pmed.0020161.txt-          [http://www.ncbi.nlm.nih.gov/UniGene/clust.cgi?ORG=Hs&CID=2159; bone sialoprotein
./technical/plos/pmed.0020161.txt-          (Hs.518726 [http://www.ncbi.nlm.nih.gov/UniGene/clust.cgi?ORG=Hs&CID=518726;
./technical/plos/pmed.0020161.txt:          bone-specific alkaline phosphatase (Hs.75431
./technical/plos/pmed.0020161.txt-          [http://www.ncbi.nlm.nih.gov/UniGene/clust.cgi?ORG=Hs&CID=75431; collagen II
./technical/plos/pmed.0020161.txt-          (Hs.408182 [http://www.ncbi.nlm.nih.gov/UniGene/clust.cgi?ORG=Hs&CID=408182; forkhead
```

Explanation: The -C n (with n being a positive integer) finds and returns all lines and n lines before and after the result that contain the designated pattern (in this case 1 line before and after "second tower" for all txt files in the 911report directory and 2 lines before and after "potassium" for all txt files in the plos directory). This would be of similar use to the -e option, except it will provide greater context to the text, and for code, it would help understand why a certain line of code was written. 
