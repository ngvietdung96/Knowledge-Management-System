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
	- Linux, MacOS: package `gpg` and  login `pass`:
		- https://www.dantuck.com/article/GnuPG-and-Pass/
	-  SSH:
		- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh
		- Test ssh connection: `ssh -T git@github.com`
			- response: `Hi user! You've successfully authenticated, but GitHub does not provide shell access.`
		-  Change remote url: 
			`git remote set-url origin git@github.com:username/your-repository.git`
	- GPG asymmetric key:
		- https://md8-habibullah.github.io/GPG-keys-with-GitHub/
		- Same guide from github:
			- [Generating a new GPG key](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)
			- [Telling Git about your signing key](https://docs.github.com/en/authentication/managing-commit-signature-verification/telling-git-about-your-signing-key)
		- Step of gpg authentication:
			- generate asymmetric key `gpg --full-generate-key
			- list current gpg key `gpg --list-secret-keys --keyid-format=long`
			- (option) gpg change uid
				- access key`gpg edit-key <key ID>`
				- add uid with user and email `adduid`
				- delete key: chose uid `uid <number>` and `deluid <number>`
			- get public format key `gpg --armor --export <key ID>`
			- add gpg public key to GIT server.
			- change git config for using signing key:
				- `git config --local credential.credentialStore gpg`
				- `git config --local user.signingkey <key ID>`
				- `git config --local commit.gpgsign true`
				- `git config --local tag.gpgsign true`
			- sign for each tag or commit
				- https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work
				- https://github.com/jesseduffield/lazygit/discussions/3738
				- debug `git log --show-signature -1`
	- Personal access tokens (classic):
		`git remote set-url orgin https://<token>@github.com/<username>/<repo>`

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