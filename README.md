# Minecraft server on rasberry pi
If you play minecraft and have a spare rasberry pi in your collection then it's always a way to do something with it. Server won't be as good as hypixel or so but for you and ur friends that'll do just well

# Installation proces

``Entire proces was made on rasberry pi 1 b+, but it'll work just well on any of the pi family. Os was dietpi, but'll work same on rasberry pi os. Server will be set up by using additional laptop with windows installed (ssh)``

## Java
Java is a must have to set up a minecraft server, it's a condition we need to install first (remember to check if the java vers you install will work well with mc version you want on your server). For this tutorial we're using java 17. To install that we first should check if our system is updated well by:
```sudo apt update```

Then we can install the java itself. On dietpi the process is a lot easier cuz we can just use **dietpi-software** by typing
```dietpi-software```
and then searching for **java** in the search box, it should pop up easily.

On any other os you can install it manually by typing:
```sudo apt install openjdk-17-jdk```

## Server setup
As mentioned earlier we'll do it on regular PC first, then just push it to our pi with ssh.

1. **Set up a folder for ur server to be in**: make a folder
2. **Download server jar**:
