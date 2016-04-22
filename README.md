# How to spin up a Virtual Machine using Vagrant

This Readme guides you through creating a Virtual Machine using Vagrant.

### Basic installation

First, you need to download VirtualBox at https://www.virtualbox.org/wiki/Downloads and install it.

Then, download Vagrant at https://www.vagrantup.com/downloads.html (v1.8.1) and install.

To check if we successfully installed vagrant on our system we can run up a command on our terminal by typing.

```bash
    vagrant version
```
The version should pop up, if not we need to log out, log back in and try again.

### Picking a vagrant box

One of the major decisions we have to make is to pick out vagrant box we are going to use. It is going to serve as your virtual OS. In my assignment i am using "Ubuntu Server 14.04 LTS". You need to pick vagrant box of your own preference. You can do that on the official hashicorp website.

* https://atlas.hashicorp.com/boxes/search

The other useful website for vagrant boxes is

* http://www.vagrantbox.es/

For "Ubuntu Server 14.04 LTS" we need the full name of the box. Name of the box is "ubuntu/trusty64".

### Starting up

We have to chose a path where we are going to install our Vagrant. By doing that we need to create our project folder and navigate to it. We can do that in our terminal by typing a command: 

```bash
    cd C:\Users\Kenan\Desktop\Vagrant   #You need to put your own folder path
```


After that you need to run a command in your terminal 
```bash
    vagrant box add ubuntu/trusty64     #You are putting your own box name
```
This will fetch your box directly from the catalog of vagrant images.

Then we need to create our initial vagrant file, and initialize our current directory to be a Vagrant environment. We are doing that by typing a command:

```bash
    vagrant init ubuntu/trusty64     #You are putting your own box name
```

After running a command you get a message on your terminal saying:

```bash
    A `Vagrantfile` has been placed in this directory. 
    You are now ready to `vagrant up` your first virtual environment! 
    Please read the comments in the Vagrantfile as well as documentation 
    on `vagrantup.com` for more information about using Vagrant.
```

Now we have to type:

```bash
    vagrant up
```

This is the command we use to start up our Virtual Machine, and it creates and configures guest machines according to our Vagrant file.

All we have to do now is to type:

```bash
    vagrant ssh
```
Now we are in our Ubuntu 14.04 Server, and we have access to a shell.
