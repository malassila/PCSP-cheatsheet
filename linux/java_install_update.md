# Java in Linux

<!-- Overview of the file -->
This Markdown file provides a comprehensive guide for managing Java and related tools on Arch Linux and Arch based distros.

<!-- Table of Contents -->
- [Java in Linux](#java-in-linux)
    - [To check if Java is installed:](#to-check-if-java-is-installed)
    - [To install Java on Arch based distros:](#to-install-java-on-arch-based-distros)
    - [Find all the packages of a specific version:](#find-all-the-packages-of-a-specific-version)
  - [To uninstall Java:](#to-uninstall-java)
- [](#)
- [Setting the Default Java Version](#setting-the-default-java-version)
- [](#-1)
- [Installing Maven](#installing-maven)



### To check if Java is installed:
```bash
java -version
```

### To install Java on Arch based distros:
```shell
sudo pacman -S jre17-openjdk-headless jre17-openjdk jdk17-openjdk openjdk17-doc openjdk17-src
```

### Find all the packages of a specific version:
```shell
pacman -Q | grep 'jdk11\|jre11'
```
## To uninstall Java:
Uninstall all the returned packages from the previous command:
```shell
sudo pacman -R jre11-openjdk-headless jre11-openjdk jdk11-openjdk openjdk11-doc openjdk11-src
```
#
# Setting the Default Java Version
Arch Linux provides a script archlinux-java to manage installed Java environments. To set the default Java version, first list all installed Java environments:

```shell
archlinux-java status
```

Then set the default Java version by replacing <JAVA_ENVIRONMENT> with the name of the Java environment:

```shell
sudo archlinux-java set <JAVA_ENVIRONMENT>
```
#
# Installing Maven
```shell
sudo pacman -S maven
```

