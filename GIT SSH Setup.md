# GIT SSH Setup

An SSH key is an access credential for the SSH (secure shell) network protocol. This authenticated and encrypted secure network protocol is used for remote communication between machines on an unsecured open network. SSH is used for remote file transfer, network management, and remote operating system access. The SSH acronym is also used to describe a set of tools used to interact with the SSH protocol.

SSH uses a pair of keys to initiate a secure handshake between remote parties. The key pair contains a public and private key. The private vs public nomenclature can be confusing as they are both called keys. It is more helpful to think of the public key as a "lock" and the private key as the "key". You give the public 'lock' to remote parties to encrypt or 'lock' data. This data is then opened with the 'private' key which you hold in a secure place.

https://help.github.com/en/enterprise/2.15/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
https://help.github.com/en/enterprise/2.15/user/articles/checking-for-existing-ssh-keys
https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account

### Install Git
https://git-scm.com/download

Note: Please make sure you have installation rights.

---

## Generating a new SSH key 

Open Git Bash.

Paste the text below, substituting in your GitHub Enterprise email address.

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

This creates a new ssh key, using the provided email as a label.

Generating public/private rsa key pair.

When you're prompted to `Enter a file in which to save the key,` press Enter. This accepts the default file location.

Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]

At the prompt, type a secure passphrase

Enter passphrase (empty for no passphrase): (leave it blank)

Enter same passphrase again: (leave it blank)

Adding a new SSH key to your GitHub account

Enter `ls -al ~/.ssh` to see if existing SSH keys are present:

Lists the files in your .ssh directory, if they exist


Copy the SSH key to your clipboard.

If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.

`clip < ~/.ssh/id_rsa.pub`

Copies the contents of the id_rsa.pub file to your clipboard

In the upper-right corner of any page, click your profile photo, then click Settings.

In the user settings sidebar, click SSH and GPG keys.	

Click New SSH key or Add SSH key.

In the "Title" field, add a descriptive label for the new key.

Paste your key into the "Key" field.

Click Add SSH key.

If prompted, confirm your GitHub Enterprise password.

Clone the Repository

git clone "ssh clone repo link" (Run this through command prompt for first time)

You might get a mesasge for first time you run any git command.. `the authenticity oh host http://proxy.company.com can't be established. ... are you sure you wwant to continue connecting (yes/no)?`

Type yes

And it will not ask you same question again unless you format your system.

Now you can configure GIT in your choice of IDE (VS Code is recommended).
