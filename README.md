# MINIGREP

A simple grep made in Rust.



# Building

```
cargo build --release
```

This builds the manifest executable in `\\target\release\` directory. 



# Uses

`.\minigrep expression-to-search file-name `

You can also set an environment variable `CASE_INSENSITIVE` to indicate if you want the search to be case sensitive or not.

To set the case insensitive flag, you can use `$ENV:CASE_INSENSITIVE=1`.

## Examples

Suppose we have file called `sometext.txt` having contents:

```
There is some text.
So much to see,
so I go out everyday.
But I can't look out much.
```

And we want to search for `so`.

We can do so by

  `.\minigrep so sometext.txt`.

The output we will get is:

```
There is some text.
so I go out everyday.
```

To search in all cases, we can write 

`$ENV:CASE_INSENSITIVE=1; .\minigrep so sometext.txt`

```
There is some text.
So much to see,
so I go out everyday.
```



# Features to Add

- User should be able to pass case checks through arguments.
- Text should be highlighted where the string has been matched.



