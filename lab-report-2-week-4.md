# Week 4 Lab 2

## Code Change #1
![Test case1](https://user-images.githubusercontent.com/98373624/164944133-caf34151-80bd-4134-8490-d28f3376c956.png)

Link to first [Failure-Inducing Input](https://github.com/magikarp620/markdown-parser/blob/main/test-file.md?plain=1)

Symptom of failure-inducing input: __infinity loop__

The test file contains a empty element in the last line causing the current index unable to increment past the length of the file, therefore causing the infinity loop.  
![failure-output](https://user-images.githubusercontent.com/98373624/164944073-c4fb247f-4470-44a1-9c2c-98a7560b6075.png)

We added a break statement to solve this problem, if the next element is not found the indexOf function returns -1, and if the open bracket index equals -1 we break the loop.  
![codeChange1](https://user-images.githubusercontent.com/98373624/164943379-6d86d88d-488b-460a-96bc-913d16465312.png) 
link to [code change#1](https://github.com/magikarp620/markdown-parser/commit/8869f55d8f9757d433940ead9087dd1a0d2d4bc4)
## Code Change #2
![Test case2](https://user-images.githubusercontent.com/98373624/164944428-0fc5caba-15e6-41e7-afc8-c96898942d8b.png)  
Link to second [Failure-Inducing Input](https://github.com/magikarp620/markdown-parser/blob/main/test-file2.md?plain=1)

Symptom of failure-inducing input: wrong output

When the input type is Images/images the function still output the name of the file.
![failure-output2](https://user-images.githubusercontent.com/98373624/166506106-7d1e40c1-6b1d-4af5-a674-eaeb13139a90.png)


We limited image output by checking the file type, if it equals images or Images, we avoid from returning the string 
![codeChange2](https://user-images.githubusercontent.com/98373624/164944611-5289e5c3-1314-4811-9889-f7cc66cd072b.png)
link to [code change#2](https://github.com/magikarp620/markdown-parser/commit/11690faf09e29d19b31dd8b4fb8620692641dced)
## Code Change #3
![Test case3](https://user-images.githubusercontent.com/98373624/164944655-fed0da2d-5bd7-4dea-97a4-641e42adc5cc.png).   
Link to third [Failure-Inducing Input](https://github.com/magikarp620/markdown-parser/blob/main/test-file4.md?plain=1)

Symptom of failure-inducing input:
```
Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 2
```

When the input file only contains a pair of bracket without the parenthesis, the index out of bound exception occurs because the indexOf("(") function return -1 and the substring method tried to use the index.
![failure-output3](https://user-images.githubusercontent.com/98373624/164944766-26dc1cda-a774-4768-b186-c6468ac21e0b.png)

We added a similar code change to change #1 avoid takeing the substring when parenthesis are not found
![codeChange3](https://user-images.githubusercontent.com/98373624/164944829-98dbe83a-bd8c-4384-bd85-669754a54e0e.png)
link to [code change#3](https://github.com/magikarp620/markdown-parser/commit/a1c170289c37b1f8594b1c3bc30d80be44e8252a)
