Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Version Control System (VCS)]]

---
## Git credential
- https://github.com/git-ecosystem/git-credential-manager
	- Cross-platform: Linux, WindowOS, MacOS
	- It aims to provide a consistent and secure authentication experience, including multi-factor auth, to every major source control hosting service and platform
- [Install instruction - git doc](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md)
- [Credentail stores - git doc](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/credstores.md)
	- Linux, MacOS: package `gpg` and `pass`.
	- `git config --global credential.credentialStore gpg`


## Git configuration
- 3 types of configuration level: `--system`, `--global` and `local`
	- command: `git config -l --show-origin`
- EOL different between platform:
	- [Configuring Git to handle line endings - doc.github](https://docs.github.com/en/get-started/git-basics/configuring-git-to-handle-line-endings)
	- [What's the strategy for handling CRLF (carriage return, line feed) with Git?](https://stackoverflow.com/questions/170961/whats-the-strategy-for-handling-crlf-carriage-return-line-feed-with-git)


## Git workflow
Git Clone Specific Tag
- `git clone --branch <tag_name> <repository_url>`



---
# References
Official website:
Wikipedia:
Youtube: