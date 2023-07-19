# Tutorial to set up virtual workstation in your GCP project (for beginner)
In this tutorial we will go through how to set up a Linux virtual desktop. 

For reference here is the google guide on creating virtual workstations on GCP: https://cloud.google.com/compute/docs/virtual-workstation

Here is table lists options for creating a virtual workstation. Note that if you wish to use the first 2 configurations of virtual workstation, you would need to install a Teradici [Zero Client](https://www.teradici.com/products/desktop-performance-solutions/zero-clients) or the latest [Teradici software client](https://docs.teradici.com/find/product/software-and-mobile-clients) for Windows, Mac, or Linux to access the virtual workstation. You would also need a Teradici Cloud Access Software license. 
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/31d6ad13-4cd8-4bf9-bb6f-466381453bac)

Preconfigured virtual workstation solution on [Cloud Marketplace](https://console.cloud.google.com/marketplace) are available if you don't want to use the configurations in the table above
![image](https://github.com/PHACDataHub/Wiki/assets/133695429/21f5068e-23fc-428d-ac3a-212869bc1da9)


## 1. set up your gcp virtual machine
here is the guide that google provides to set up virtual machine if you are not familiar with using google cloud shell.
https://cloud.google.com/compute/docs/instances/create-start-instance

Following the google guide we will arrive at the new VM instance configuration page. One thing to note is that boot disk determines what operation system and distribution the VM will be in.
## ![image](https://github.com/PHACDataHub/Wiki/assets/133695429/4a62ffb4-2da8-4423-9b48-9f07eb099b5a)


## 2. ssh into the virtual machine an
