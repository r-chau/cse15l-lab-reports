# Lab Report 4

> **Snippet 1**

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

Using VSCode preview, this is what the above markdown file should produce:

`` `google.com``

`google.com`

`ucsd.edu`

> **Snippet 2**

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

Using VSCode preview, this is what the above markdown file should produce:

`a.com`

`a.com(())`

`example.com`

> **Snippet 3**

```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

Using VSCode preview, this is what the above markdown file should produce:

`https://www.twitter.com`
`https://ucsd-15l-w22.github.io/`
`https://cse.ucsd.edu`