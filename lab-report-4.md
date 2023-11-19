Lab Report 4
============
_Enrique Aranda_

Time: Less than 2 minutes

Step 4:
Command line: 
``` cpp
  ssh cs15lfa23os@ieng6.ucsd.edu
```

This is to log into my ieng6 account. 

Step 5: 
Command line: 
``` cpp
  git clone https://github.com/ucsd-cse15l-s23/lab7
  cd lab7
```

This is to clone my fork of the repository. Then, you change directory into the `lab7` directory.


Step 6:
Command line:
``` cpp
  bash test.sh
```

The bash command runs the test script, and the results show that they fail.


![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/45360325-150b-4bb3-aae2-295c188e5fe1)



Step 7:
Command line:
``` cpp
  vim ListExamples.java
```

The vim command is to enter into editing the `ListExamples.java` file.

Keys pressed:
``` cpp
<ESC>
</index1>
<n> <n> <n> <n> <n> <n> <n> <n>
<l> <l> <l> <l> <l> 
<x>
<i>
<2>
<ESC>
<:wq>
```

The `</index1>` is meant to scroll through all the times 'index1' is mentioned throughout the file, it takes 8 `n` presses to get to the one that needs to be changed. 
Then, you press `l` 5 times in order to get to the end of the index1 and then you replace the 1 with a 2 using the `x` and `i` commands.
At last, you press `<ESC>` and then `<:wq>` in order to save and quit.


Step 8:
Command line:
```cpp
  bash test.sh
```

Run `bash` again in order to see that `ListExamples.java` has now passed the tests.

Step 9: 
Then go to the forked repository and press commit on the Github account to commit and push the files.




