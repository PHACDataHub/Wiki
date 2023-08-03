## Steps to setup your Yubikey
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

_make note of install path, we will use part of it for the next step _

Add yubikey-manager to system path in powershell(temp)

Set PATH variable, search the start menu for "path"

![image](https://github.com/PHACDataHub/Wiki/assets/367922/004b00f6-a149-4f12-8014-5a7f56a852c6)

![image](https://github.com/PHACDataHub/Wiki/assets/367922/ea777b4d-681f-478c-bf98-cf1346098c56)

![image](https://github.com/PHACDataHub/Wiki/assets/367922/8d7144fd-c23b-4be6-8141-38b6f8d3316e)

Add path value c:\users\ _**username**_ \appdata\roaming\python\python310\Scripts
