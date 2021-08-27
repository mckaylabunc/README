# README
New User README

## Setting Up SSH Keys
Github no longer permits password access withouth 2FA to access all resources
most importantly the ability to push/pull from the remote. 
You can either:
	- setup 2FA with your github account
	- use personal access tokens
	- use SSH keys -- Recommended 

[Github SSH Key Instructions](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

### OSX
- Check if you have existing SSH keys
1. Open Terminal and enter `ls -al ~/.ssh`
	- you're looking for `id_rsa.pub` -- a public SSH key
	- if yes, there should be matching `id_rsa` file -- the private SSH key of the pair
		* never share a private key!	
	- Go to step 3

2. If you don't have an existing keypair -- generate a new one
	- Open Terminal and enter `ssh-keygen`
		- You'll be prompted to enter a filename -- Not necessary, just hit enter. 
		- You'll be prompted to enter a password -- Also not necessary, just hit enter.
		- This generates a default SSH keypair - a "public" key `id_rsa.pub` and a "private" key `id_rsa`  
	 		- The private key should always be kept secure and not shared, but the public key can be shared freely 

3. Share your public key with Github
	- Go to your Github account settings
	- Then "SSH and GPG Keys"
	- Click "New SSH key" - add a Title, such as the nickname for the local machine you're using  
	- Copy and paste the `id_rsa.pub` key then click "Add SSH key"

4. You'll need to do this for each machine you use to work with github -- adding a different public key to your account for each
