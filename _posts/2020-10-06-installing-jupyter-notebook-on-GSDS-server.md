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
$ bash ~/{the directory of Anaconda installer}/Anaconda3-2020.02-Linux-x86_64.sh
```

### Initial Setting
- Notations:
  - ***ID***: manapool
  - ***server_IP***: 147.47.200.22
  - ***local_port***: 8001 (or 8004)
  - ***server_port***: 8889 (or 8899)
  - ***gpu_server***: gpu02 (or gpu04)
  - ***gpu_port***: 8889 (or 8899)
- We are going to use two terminals.
- Open a first terminal from Windows 10 and type:

```
> ssh -fN {ID}@{server_IP} -L {server_port}:localhost:{local_port}
```

- Open a second terminal from Windows 10 and type:

```
> ssh {ID}@{server_IP}
> ssh -f {gpu_server} -L {gpu_port}:localhost:{server_port} -N -K
```

### Using Putty to Access Jupyter Notebook
- Open PUTTY and input the ***server_IP*** as the Host Name
- Set Port as **22554**

![fig1](/assets/fig/2020-10-06-installing-jupyter-notebook/fig1.jpg)

- Go to SSH on the bottom of the left pane to expand the menu and then click on Tunnels
- Input ***local_port*** in Source Port and ***server_port*** in Destination as follows:

![fig2](/assets/img/2020-10-06-installing-jupyter-notebook/fig2.jpg)

- Save Putty session (through Change Settings)
- Login to the GSDS server using the saved session.
- Now you can access Jupyter Notebook through the following cli:

```
# login GSDS server with saved Putty session
$ ssh gpu02 (or gpu04)
$ jupyter notebook --port=8889 (or 8899)
```

- Server will notice you that Jupyter Notebook is running.
- Type in your browser `localhost:{local_port}` to use Jupyter Notebook

### cf. How to kill a specific port - [LINK](https://brocess.tistory.com/82)



