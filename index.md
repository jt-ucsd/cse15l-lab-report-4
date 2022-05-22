# Lab Report 4
--

By: jt

Link to My MarkdownParser: [My Markdown Parser](https://github.com/jt-ucsd/markdown-parser)
* Specific Link to the MarkdownParser version I created and used: [Markdown Parser Used](https://github.com/jt-ucsd/markdown-parser/commit/00c390a2476a6e5a84d99137a5ac92d3df82823a)

Link to Peer's MarkdownParser: [Peer's Markdown Parser](https://github.com/ujik500/markdown-parser)

## Snippet 1

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

1. It should produce [`google.com].

2. Test for Snippet One:

![Snippet 1 Test](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Test%20for%20Snippet%20One.JPG)

3. My MarkdownParse:

![Snippet 1 Test Personal](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%201%20Main%20Fail.jpg)

4. Reviewed Markdown Parse: 

![Snippet 1 Test Peer](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%201%20Peer%20Fail.jpg)

## Snippet 2

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

1. It should produce `[a.com, a.com(()), example.com]`.

2. Test for Snippet Two:

![Snippet 2 Test](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Test%20for%20Snippet%20Two.JPG)

3. My MarkdownParse:

![Snippet 2 Test Personal](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%202%20Main%20Fail.jpg)

4. Reviewed Markdown Parse: 

![Snippet 2 Test Peer](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%202%20Peer%20Fail.jpg)


## Snippet 3

```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

1. It should produce `[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]`.

2. Test for Snippet Three:

![Snippet 3 Test](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Test%20for%20Snippet%20Three.JPG)

3. My MarkdownParse:

![Snippet 3 Test Personal](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%203%20Main%20Fail.jpg)

4. Reviewed Markdown Parse: 

![Snippet 3 Test Peer](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-4/main/Snippet%203%20Peer%20Fail.jpg)

## Question Responses:

1. I will have to make a larger code change than 10 lines in order to come up with a logic that appropriately ignores ` when applicable.

2. I will be able to make a change in fewer than 10 lines because, I would just need to count how many `[` brackets are there before the first `]` and skip the appropriate number.

3. I will be have to make a change of more than 10 lines because, there will be situations where I want to ignore new line and situations where I don't.  If I just wrote a few lines combining all of the lines into a single long string, there will be test cases where it fails because, the previous line ends with a `!`.