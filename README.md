# test
test git clone on cygwin.
1. Run setup.exe for cygwin
2. Add git related packages, add openssh, add GnuPG
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
