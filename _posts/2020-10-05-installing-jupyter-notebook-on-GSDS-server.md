---
layout: post
title: Installing Jupyter Notebook on GSDS Server and Accessing It through Putty from Windows 10
excerpt_separator:  <!--more-->
categories:
  - Server
tags:
  - Jupyter Notebook
  - Server
---

### Prerequesits
- A GSDS server account
- GSDS **server_IP**: 147.47.200.22 **port**: 22554
- FileZilla (to send files to GSDS server)
- Install Putty on Windows 10

<!--more-->

### Installing Jupyter Notebook on GSDS Server
- Download recent Linux ver. Anaconda installer - **[link](https://docs.anaconda.com/anaconda/install/linux/)**  
*At Oct 6, 2020, the most recent Anaconda installer ver. is*<br> 
*Anaconda3-2020.07-Linux-x86_64.sh*
- Use Filezilla and send Anaconda installer to GSDS server
- Login GSDS server using Putty and install Anaconda

```
> bash ~/{the directory of Anaconda installer}/Anaconda3-2020.02-Linux-x86_64.sh
```

### Initial Setting
- Notations:
  - ***ID***: manapool
  - ***server_IP***: 147.47.200.22
  - ***local_port***: 8001
  - ***server_port***: 8889
  - ***gpu_server***: gpu02
  - ***gpu_port***: 8889
- Open a terminal from Windows 10 and type:

```
> ssh -fN {ID}@{server_IP} -L {server_port}:localhost:{local_port}
```

- Open a new terminal from Windows 10 and type:

```
> ssh {ID}@{server_IP}
> ssh -f {gpu_server} -L {gpu_port}:localhost:{server_port} -N -K
```

- Open a third terminal and run:

```
>ssh -X {ID}@{server_IP}
>ssh -KX {gpu_server}
>jupyter notebook --no-browser --port=8889
```

- type in a browser `localhost:{local_port}` and check if you can access Jupyter Notebook

### Using Putty to Access Jupyter Notebook
- Open PUTTY and input the ***server_IP*** as the Host Name
- Set Port as **22554**

![img1](/assets/img/201006_img1.jpg)

- Go to SSH on the bottom of the left pane to expand the menu and then click on Tunnels
- Input ***local_port*** in Source Port and ***server_port**** in Destination as follows:

![img2](/assets/img/201006_img2.jpg)

- Click Open and login GSDS server
- Open Jupyter Notebook

```
$ ssh gpu02
$ jupyter notebook --no-browser --port=8889
```

- type in a browser `localhost:{local_port}` to use Jupyter Notebook
- save Putty session (through Change Settings) for convenient access next time

