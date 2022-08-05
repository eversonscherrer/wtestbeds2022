# wtestbeds2022
Official repository for the paper to WTESTBEDS - 1º Workshop de Testbeds

# Overview
This repository has all the files needed to run the topology and which was put as an example in the article "FreeRouter in a Nutshell: A "Protocoland'' routing platform for Open and Portable Carrier-Class Testbeds" sent to WTESTBEDS - 1st Testbeds Workshop.

# Freertr
Freertr is a control plane: Router OS process speaks various network protocols, (re)encap packets, and exports forwarding tables to hardware switches. Basically, it is only necessary to install the Java Runtime Environment (JRE). Below is demonstrated how to install it on operating systems: Linux, Windows and macOS.

## Install JRE
### Linux
For demonstration purposes, the Debian-based Linux installation was chosen.
```console
#sudo apt-get install default-jre-headless --no-install-recommends
```

### MacOS
```console
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
sdk list java
sdk install java 17.0.2-open
sdk default java 17.0.2-open
java -version
```

### Windows
In order to install the Windows version of Java, you need to visit the official Java website and download the Windows executable. After the download, check if your user has permission to install and perform the installation through the graphical environment. 

## Install Freertr
The freeRouter homepage is at freertr.net. Starting from this page, you'll find various resources such as source code (there is also a GitHub mirror), binaries, and other images that might be of your interest. From there we just download the freeRouter jar files.

```console
#wget freertr.net/rtr.jar
````

# Launch the Topology
Now it's time to run the topology, to run it, download all the hardware and software files that are in the repository, in the same folder.

**NOTE**
> To orchestrate the execution of the topology we use ```tmux```, if you don't have it installed, remember to install it.
```console
sudo apte-get install tmux
or
brew install tmux
````

# Full Mesh Topology

![wtestbeds](https://user-images.githubusercontent.com/56919528/162601454-0ba62c51-5d74-40b5-8507-03c1e59f7d6d.png)


## To run topology
Edit the ```star-topology.sh``` file.
```console
vim start-topology.sh
````
This file has two environment variables ```$STR``` and ```$HWSW```, add the path according to your operating system.

### Run
```console
./start-topology

```
# Troubleshooting

## Accessing by Telnet 
To access routers by telnet use ```telnet <ip address> <port>```.

For Example:
Accessing Router R1

```console
telnet 127.0.0.1 1123
````

## Verifying the interfaces is working on router r1

```console
R1# Show interfaces summary
````

## Visualizing route table r1
```console
R1# show ipv4 route v1
````

## Testing connectivity between R1 to R3

```console
R1# ping 6.6.6.1 /vrf v1
````

## Verifying trace between R1 to R3

```console
R1# traceroute 6.6.6.1 /vrf v1
````

## This is our presentation

![pdf](https://github.com/eversonscherrer/wtestbeds2022/blob/main/FreeRouter%20in%20a%20Nutshell_%20A%20%E2%80%9CProtocoland%E2%80%9D%20routing%20platform%20for%20Open%20and%20Portable%20Carrier-Class%20Testbeds.pdf)


## Cite this work

Bibtex:

```bibtex
@inproceedings{wtestbeds,
 author = {Everson Borges and Edgard Pontes and Csaba Mate and Frederic Loui and Magnos Martinello and Moisés Ribeiro},
 title = {FreeRouter in a Nutshell: A "Protocoland" routing platform for Open and Portable Carrier-Class Testbeds},
 booktitle = {Anais do I Workshop de Testbeds},
 location = {Niterói},
 year = {2022},
 pages = {36--46},
 publisher = {SBC},
 address = {Porto Alegre, RS, Brasil},
 doi = {10.5753/wtestbeds.2022.223341},
 url = {https://sol.sbc.org.br/index.php/wtestbeds/article/view/20752}
}
````

