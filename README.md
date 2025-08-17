## Guide to uninstall Java from Ubuntu system 

- Copy & paste the below commands to terminal >
```
    java --version
    javac --version
    sudo -i
    dpkg-query -W -f='${binary:Package}\n' | grep -E -e '^(ia32-)?(sun|oracle)-java' -e '^openjdk-' -e '^icedtea' -e '^(default|gcj)-j(re|dk)' -e '^gcj-(.*)-j(re|dk)' -e '^java-common' | xargs sudo apt-get -y remove
    apt autoremove
    apt update
    apt upgrade -y
    apt update
    rm -rf /usr/lib/jvm/*
    java --version
    javac --version
```