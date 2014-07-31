Content goes here...test-repo
=========
Test of built-in markdown syntax-highlighting.

```bash
   for f in fgh*; do mv $f $(echo $f | sed 's/^fgh/jkl/g'); done
```

For testing purposes.

#Source SDK 2013
Get via
```bash
   git clone git@github.com:ValveSoftware/source-sdk-2013.git
```

Next, 
```bash
   # Single Player Project
   $SDK_ROOT/sp/src/creategameprojects
   $SDK_ROOT/sp/src/createallprojects

# Multiplayer Project
   $SDK_ROOT/mp/src/creategameprojects
   $SDK_ROOT/mp/src/createallprojects
```

On Linux, do the following:
Extract the steam runtime:
```bash
   $ tar xvf steam-runtime-sdk_latest.tar.xz
   $ cd steam-runtime-sdk_<version>
```
Now, run 
```bash
   $ ./setup.sh
```

Pick your architecture and debug/release preferences. Then answer Y to everything else.

```bash
   $ ./shell.sh --arch=i386
```

#ON MAC OS X

All you do is run
```bash
   $ make -f games.make
```
