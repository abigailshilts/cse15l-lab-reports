# Week 7 and 8 lab report

[My repository](https://github.com/abigailshilts/markdown-parse-group)
[Reviewed repository](https://github.com/yi113/markdown-parse)

## Code snippet 1:

When the original code snippet is opened in a VScode preview ie looks like:
![Image](img4/test1-expected.png)

Thus the expected output is [google.com, google.com, ucsd.edu]

To test this I added this test to MarkdownParseTest:

![Image](img4/test-snippet1.png)

This test failed when run against my version of MarkdownParse with this output:
![Image](my-failure1.md)

This test also failed when ran against the version of markdown parse reviewed during my lab with this output:
![Image](other-failure1.md)

The fix for this would not be considered a small change. For every new open bracket found tou would need to loop through the substring between the current index and the open bracket to detirmine how many back ticks existed. If it was an even number then you could use the link if not then the link was invalid. However it gets more complex in that you have to check that the backticks occur on the same line as the new open bracket in which case you have more comparisons to detirmine where to begin to check the substring for backticks or where to end it. Each of these loops and comparisons would be more than 3 lines. After that you then also have to remoev all back ticks from all valid links which is also another line of code. All together it will end up being >10 lines.