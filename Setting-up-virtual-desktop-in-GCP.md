# Tutorial to set up virtual workstation in your GCP project (for beginner)
In this tutorial we will go through how to set up a Linux virtual workstation, specifically setting up chrome remote desktop in Debian distribution following this google guide: https://cloud.google.com/architecture/chrome-desktop-remote-on-compute-engine

_For reference here is the general google guide on creating virtual workstations on GCP: https://cloud.google.com/compute/docs/virtual-workstation_

_Please check the general google guide to make sure you have all the pre-requisite_

Here is a table listing options for creating a virtual workstation. Note that if you wish to use the first 2 configurations of virtual workstation, you would need to install a Teradici [Zero Client](https://www.teradici.com/products/desktop-performance-solutions/zero-clients) or the latest [Teradici software client](https://docs.teradici.com/find/product/software-and-mobile-clients) on your local machine to access the virtual workstation. You would also need a Teradici Cloud Access Software license. 

![image](https://github.com/PHACDataHub/Wiki/assets/133695429/31d6ad13-4cd8-4bf9-bb6f-466381453bac)

Preconfigured virtual workstation solution on [Cloud Marketplace](https://console.cloud.google.com/marketplace) are available if you don't want to use the configurations in the table above
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/21f5068e-23fc-428d-ac3a-212869bc1da9)


## 1. set up your gcp virtual machine
here is the guide that google provides to set up virtual machine.
https://cloud.google.com/compute/docs/instances/create-start-instance

Following the google guide we will arrive at the new VM instance configuration page. One thing to note is that boot disk determines what operating system and distribution the VM will be in.
## ![image](https://github.com/PHACDataHub/Wiki/assets/133695429/4a62ffb4-2da8-4423-9b48-9f07eb099b5a)


## 2. ssh into the virtual machine and install chrome remote desktop
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/65da4fd7-1347-4e8f-b6db-94c18f03345f)

## 3. install desktop environment for our linux vm
Here is some common option that google recommend:
* [Xfce](https://www.xfce.org/)
* [Cinnamon](https://www.linuxmint.com/)
* [Gnome](https://www.gnome.org/)
* [Gnome-Classic](https://help.gnome.org/users/gnome-help/stable/gnome-classic.html.en)
* [KDE Plasma](https://kde.org/)

The google guide will provide the linux commands for installing the common desktop environment mentioned about. Strongly recommend doing the optional step as well, and reboot the vm after installation of desktop environment finishes. One quick way to reboot vm is to type `sudo reboot` in the ssh window
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/054c0a5b-17f7-4902-8527-ba3a410dedc7)

## 4. configure remote desktop service
Go to https://remotedesktop.google.com/headless, on the left hand side go to **set up via ssh** tab. Click begin to start the set up process, which involves 3 steps. If you downloaded and install the chrome-remote-desktop deb file in the previous step, then you can ignore the first step in the set up process. Step 2 is authorization, and step 3 involves copy and pasting the remote desktop configuration command google provided into your new vm's ssh window.

you can paste these commands in your ssh window for verification 
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/b7d8e3a4-560d-478f-9e98-ed16d3fdcb40)

After finishing the set up process, if you go back to the **remote access** tab on the left hand side, the new vm should appear. like below
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/8cb1e317-221b-4e1b-8150-700ff58ce1fd)

click on the icon with your vm name will initiate connection to your new virtual desktop. It will ask you for the 6 digit pin code you just created in the step 3 of the set up process. After inputting the pin, you will be log on to your virtual desktop. Your desktop should look something similar to this
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/4647012f-ae63-4fef-8f66-edd400872f88)

## Post installation
Here are 6 post installation steps at the end of the tutorial and some troubleshooting tips to help make the virtual desktop run smoothly, highly recommended to take a look at them.

I especially recommend the following 3 post installation steps
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/c6896750-b68d-421d-866f-ae21cc030234)
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/669c8332-b03e-49ac-8728-6a611d39f26b)
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/30d94105-038d-4165-abee-ccc5d931c946)

### Please remember to turn off your virtual desktop if you are not using them for long period of time, because uptime costs money!


 


