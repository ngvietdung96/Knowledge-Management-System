Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[VirtualBox]]

---
# Case sensitive

https://learn.microsoft.com/en-us/windows/wsl/case-sensitivity

To check if a directory is case sensitive in the Windows filesystem, run the command:
```
fsutil.exe file queryCaseSensitiveInfo <path>
```

Replace `<path>` with your file path. For a directory in the Windows (NTFS) file system, the `<path>` will look like: `C:\Users\user1\case-test` or if you are already in the `user1` directory, you could just run: `fsutil.exe file setCaseSensitiveInfo case-test`


To enable case-sensitivity on a directory (FOO ≠ foo), use the command:
```
fsutil.exe file setCaseSensitiveInfo <path> enable
```

To disable case-sensitivity on a directory and return to the case-insensitive default (FOO = foo), use the command:
```
fsutil.exe file setCaseSensitiveInfo <path> disable
```

## Configure case sensitivity with Git

The Git version control system also has a configuration setting that can be used to adjust case sensitivity for the files you are working with. If you are using Git, you may want to adjust the [`git config core.ignorecase`](https://git-scm.com/docs/git-config/#Documentation/git-config.txt-coreignoreCase) setting.

To set Git to be case-sensitive (FOO.txt ≠ foo.txt), enter:
`git config core.ignorecase false`

To set Git to be case-insensitive (FOO.txt = foo.txt), enter:
`git config core.ignorecase true`

Setting this option to false on a case-insensitive file system may lead to confusing errors, false conflicts, or duplicate files.

For more information, see the [Git Config documentation](https://git-scm.com/docs/git-config/).



---
# References
Official website:
Wikipedia:
Youtube: