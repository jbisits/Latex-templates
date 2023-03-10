# Remove biber cache

I ran into a frustrating issue with bibtex and this is the way to solve it [stack exchange](https://tex.stackexchange.com/questions/140814/biblatex-biber-fails-with-a-strange-error-about-missing-recode-data-xml-file).
The command I ran (after which I think everything worked was)

```terminal
rm -rf biber --cache
```

so if it happens again this is what to try!
**If you do it this way first delete all the excess files that latex produces when it compiles.**

The next time I had corrupted cache this did not work as quickly.
I tried suggestions from [here](https://tex.stackexchange.com/questions/543837/very-strange-error-suddenly-appeared-running-biber) which still did not work.
Then I **removed all the files generated in the building of the doc and that did the trick**
I had cleared the cache so maybe that is the order of operations.

This error seems to occur with *failed builds* which then results in corrupted cahce for `bibtex`.
Hopefully that is all I have to deal with for now.
