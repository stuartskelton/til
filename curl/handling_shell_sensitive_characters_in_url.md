# Handling shell sensitive characters in URL

Sometimes you want to request an URL from the command-line, but the URL contains characters bearing meaning in your shell.

```bash
$ curl --header Accept:application/json https://USERID:funkyPassMo|)@eksempel.dk/dostuff
-bash: syntax error near unexpected token '|'
```

Simply quote the URL

```bash
$ curl --header Accept:application/json "https://USERID:funkyPassMo|)@eksempel.dk/dostuff"
-bash: syntax error near unexpected token '|'
```

And of you special character is a quote, quote differently.

See also: http://wiki.bash-hackers.org/syntax/quoting

