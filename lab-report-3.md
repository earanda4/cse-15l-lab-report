Lab Report 3
============
_Enrique Aranda_

__Part 1:__
The bug I will be focusing on is the buggy implementation of the `reverseInPlace` method of the `ArrayExamples` class:

Failure-inducing input:
```
 @Test
  public void testA(){
    int[] input1 = { 3, 2, 1 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 1, 2, 3 }, input1);
  }
```


Input that does not induce a test failure:
```
@Test
  public void testC(){
    int[] input = {1};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{1}, input);
  }
```


Symptom:

![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/f9699b2a-896e-47c9-a94a-363df43b478f)


Bug:

Before: 
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```


After:
```
 static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```


Change: 
The main fix for the bug was to add a new variable `temp` and to change the for loop to only iterate through half the list. This way, we could set `temp` to the values on the left side of the partition and set the left side to the right side and vice versa with the help of `temp`. 




__Part 2:__
4 interesting ways to use the command `find`:
1. `-type`
Filters out the type of file that you want to find. For instance, regular files would follow `find` with `f`, directories would be `d`, and links would be `l`.


ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/4a48af12-2007-4644-924c-71836c123bb8)


The `d` part of the command is filtering out the directories that are in `technical/`.

ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/63bf7983-a914-4d66-bfc9-6c22ebd35c4b)
![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/3f321ba8-55b4-426d-b2c5-8914a9b57934)


The `f` part of the command is showing only the files that are in `technical/`.


Source: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/

2. `-wholename`
If you wanted out to search for a file using its full name you would include it after the `-wholename` command.


ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/65c9318e-3434-488d-bd36-b32cbecd4537)


I typed in the exact

ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/364fb962-f6fb-480e-8a87-a2e83e4d7ed8)

Source: https://www.gnu.org/software/findutils/manual/html_node/find_html/Full-Name-Patterns.html

3. `-size`
You can filter out the find through its size. After `-size`, you include the size in bytes: (M for Megabytes, k for kilobytes, c for bytes, etc.) Adding a plus or minus before the value changes whether you want it greater than or less than the included value.


ex:![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/d95b91d2-7e40-4ad8-b14d-c4b1ce657ffd)


The `+100k` is filtering through


ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/fd84d0dc-9d01-43c8-8c36-e7409275df9f)


Source: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/

4. `-delete`
Any file that is found within the `-find` command could be deleted by adding `-delete` after it.


ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/85f8e613-3ee7-4152-ac3a-4185716337db)


ex: ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/8fcfbbf1-f581-4c8e-8b39-2fa0e530f2e4)


Source: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/



