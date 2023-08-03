⚠ Still being developed ⚠ 

https://developer.okta.com/blog/2021/07/07/developers-guide-to-gpg#back-up-your-gpg-keys

https://gist.github.com/matusnovak/302c7b003043849337f94518a71df777

# Steps to setup your Yubikey

## Environment Prep

On your laptop, install the following.
* Install Python https://www.python.org/downloads/
  * (user based install)
* Install GPG gpg4win https://www.gpg4win.org/
  * (user based install)

Open powershell from the startmenu

![image](https://github.com/PHACDataHub/Wiki/assets/367922/96b1b1a0-b3c5-4689-8764-f1ee1829e06f)

Install yubikey manager 

`pip install --user yubikey-manager`

![image](https://github.com/PHACDataHub/Wiki/assets/367922/e43b94cd-25b0-4fe8-8122-7679febc38d3)

Confirm it's installed 

`pip show yubikey-manager`

![image](https://github.com/PHACDataHub/Wiki/assets/367922/35193a65-58d8-4a7c-817e-4f914cf53dca)

_make note of install path, we will use part of it for the next step_

Add yubikey-manager to system path in powershell(temp)

Set PATH variable to load yubikey manager

`$Env:PATH += ";c:\users\ _**username**_ \appdata\roaming\python\python310\Scripts"`

![image](https://github.com/PHACDataHub/Wiki/assets/367922/12201283-db28-43fe-9ffc-feea01b132b0)


## Set Up and Configure a GPG Key 
Follow this tutorial for "Set Up and Configure a GPG Key" and "Back Up Your GPG Keys" section

https://developer.okta.com/blog/2021/07/07/developers-guide-to-gpg#set-up-and-configure-a-gpg-key

Come back after

## Enable Your GPG Key for SSH

Enable SSH support using standard sockets by updating the ~/.gnupg/gpg-agent.conf file:

MAKE SURE FILE FORMAT IS NOT IN Utf16 
https://dev.gnupg.org/T2671

`echo "enable-ssh-support" >> $env:APPDATA\gnupg/gpg-agent.conf`

`echo "use-standard-socket" >> $env:APPDATA\gnupg/gpg-agent.conf`

![image](https://github.com/PHACDataHub/Wiki/assets/367922/4f48337d-beb8-4aa6-bd83-d4e2a3a26885)


Next, you will need to find the "keygrip" for the authentication key; this is different from the key id, run:

![image](https://github.com/PHACDataHub/Wiki/assets/367922/2fe456a0-9f91-4acf-abd3-21e11d3f72bc)

Update ~/.gnupg/sshcontrol with the authentication "keygrip"; this allows the gpg-agent to use this key with SSH.

![image](https://github.com/PHACDataHub/Wiki/assets/367922/23f6d415-1234-4bc6-83b4-0e39706a5802)

