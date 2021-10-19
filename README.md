# cygwin-git: installing git commands on cygwin 
Useful instructions for a new installation of cygwin and git together. These instructions assumes a little bit of user fill in the blank during implementation. Github also provides very detailed (and useful) help pages.
1. Run setup.exe for cygwin
2. Add git related packages, add openssh, add GnuPG version 2, add vim for editor
3. update git config with usernames and email
* git config --global user.name "John Doe"
* git config --global user.email "JohnDoe@somewhere.com"
4. Generate ssh key with openssh package in cygwin
* in ~ folder of a freshly opened cygwin window
* ssh-keygen -C "JohnDoe@somewhere.com" -t rsa
* press enter to accept default file location
* cd .ssh
* vim id_rsa.pub
* copy the entire key starting with "ssh-rsa ... JohnDoe@somewhere.com"
5. Add ssh key into Github account
* Login to github.com
* user drop down > settings
* SSH and GPG keys tab
* New SSH key
* add title, paste key, and add SSH key
6. Setup new GPG key, in this case try using gpg2 command
* Navigate to add GPG key to github account
* Follow the help "generate a GPG key and add it to your account"
* Follow instructions to generate GPG key, using gpg2 command instead of gpg if needed
* Copy the generated GPG key based on instructions given on the help page
* Add the GPG key to git account
7. Store git push credential
* git config credential.helper store
* git push
* enter username and password
* if using 2FA then the password must be a personal token
* generate this personal token from settings > developer settings > personal access tokens
* click Generate new token
* add repo permission
* copy the generated token and keep it safe, this will be the password
