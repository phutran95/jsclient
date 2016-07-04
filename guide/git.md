# GIT commands

<details>
	<summary>github SSH</summary>
### generate SSH key

ssh-keygen -t rsa -b 4096 -C "email@gmail.com"
	enter file name: ~/.ssh/github_NAME
	enter passphrase: 

### Add key to the ssh-agent
- check 
	eval "$(ssh-agent -s)"
- add: 
	ssh-add ~/.ssh/github_NAME

### add ssh to github account
- copy
	cat ~/.ssh/github_NAME.pub
- paste to github > setting > ssh

4. config
- create if not existed: ~/.ssh/config (sudo vi ~/.ssh/config)
- paste:

Host github.com
User git
Port 22
Hostname github.com
IdentityFile ~/.ssh/github_NAME
TCPKeepAlive yes
IdentitiesOnly yes





//Add the GitHub to the list of authorized hosts:
ssh-keyscan -t rsa github.com > ~/.ssh/known_hosts
</details>