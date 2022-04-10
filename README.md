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
Now it's time to run the topology, to execute it, download all the hardware and software files that are in the repository, in the same folder.



