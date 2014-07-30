Content goes here...test-repo
=========
Test of built-in markdown syntax-highlighting.

```bash
   for f in fgh*; do mv $f $(echo $f | sed 's/^fgh/jkl/g'); done
```

For testing purposes.

Excerpt from :
#11.3. Counting Files in the Current Directory

To determine how many files there are in the current directory, put in
```bash
ls -1 | wc -l
```
This uses `wc` to do a count of the number of lines (`-l`) in the output of `ls -1`. It doesn't count dotfiles. Please note that `ls -l` (that's an "l" rather than a "1" as in the previous examples) which I used in previous versions of this HOWTO will actually give you a file count one greater than the actual count. Thanks to Kam Nejad for this point.

If you want to count only files and NOT include symbolic links (just an example of what else you could do), you could use 
```bash
ls -l | grep -v ^l | wc -l
```
(that's an "L" not a "1" this time, we want a "long" listing here). `grep` checks for any line beginning with "l" (indicating a link), and discards that line (`-v`).

Relative speed: "`ls -1 /usr/bin/ | wc -l`" takes about 1.03 seconds on an unloaded 486SX25 (`/usr/bin/` on this machine has 355 files). "`ls -l /usr/bin/ | grep -v ^l | wc -l`" takes about 1.19 seconds.
