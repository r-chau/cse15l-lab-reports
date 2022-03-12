


Link to the student repository I used: 

Link to the provided repository to compare to:

To find the tests that provided different results, I first had the outputs of tests in a text file by running `bash script.sh > results.txt` on each directory. This command redirects the output into the text file. Then, I ran the `diff` command below to find the tests with different results.

```
diff sri-mdparse/results.txt lab-9-mdparse/results.txt
```

By looking at the output of this command, I was able to find two tests that provided different results.

> *TEST NAME*

This is what I found after using `diff`:
![image](diff-output-1.jpg)

This tell us that on line 1062 of the `results.txt` files, the student's `markdown-parse` produces `[]`, while the provided implementation produces `[train.jpg]`.

