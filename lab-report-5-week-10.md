# Lab Report 5

Link to the student repository I used: [https://github.com/smissula/markdown-parse](https://github.com/smissula/markdown-parse)

Link to the provided repository to compare to: [https://github.com/ucsd-cse15l-w22/markdown-parse](https://github.com/ucsd-cse15l-w22/markdown-parse)

To find the tests that provided different results, I first had the outputs of tests in a text file by running `bash script.sh > results.txt` on each directory. This command redirects the output into the text file. Then, I ran the `diff` command below to find the tests with different results.

```
diff sri-mdparse/results.txt lab-9-mdparse/results.txt
```

By looking at the output of this command, I was able to find two tests that provided different results.

## **`577.md`**

This is what I found after using `diff`:

![image](diff-output-1.jpg)

This tell us that on line 1062 of the `results.txt` files, the student's `markdown-parse` produces `[]`, while the provided implementation produces `[train.jpg]`. We can find this by heading to that line in both the `results.txt` files.

Our implementation: ![image](sri-output-1.jpg)

Given implementation: ![image](joes-output-1.jpg)

This shows us that the `577.md` test file is causing the different outputs. These are the contents of `577.md`:
```
![foo](train.jpg)
```
Since this is the syntax for an image and not a link, the correct output should be just `[]`, so our group's implementation was correct. 



## **`567.md`**

This is what I found after using `diff`:

![image](diff-output-2.jpg)

This tell us that on line 212 of the `results.txt` files, the student's `markdown-parse` produces `[not a link]`, while the provided implementation produces `[]`. We can find this by heading to that line in both the `results.txt` files.

Our implementation: ![image](sri-output-2.jpg)

Given implementation: ![image](joes-output-2.jpg)

This shows us that the `567.md` test file is causing the different outputs. These are the contents of `567.md`:
```
[foo](not a link)

[foo]: /url1
```
The correct expected output for this test file should be `[]`, so the given implementation produces the correct output. 