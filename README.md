# Modded minecraft server on one board computer
If you play minecraft and have a spare rasberry pi or any other one board computer in your collection then it's always a way to do something with it. Server won't be as good as hypixel or so but for you and ur friends that'll do just fine

# Installation proces

``Entire proces was made on orange pi 4 pro but it'll work just well on any of the pc's that have armbian os installed. Server will be set up by using additional laptop with windows or linux (steps are the same)  installed (ssh). Mods will be searched through curseforge``

## SSH
The thing we'll controll our board with. We're going to do this in our windows powershell / linux terminal. We need a few informations about our board to do it tho:
- Our board ip adress
- our board username
- our board username password

Now we can connect with our board by typing from this template:
```
ssh <board username>@<board ip adress>
```

When the terminal of our board pops up, then you know you did well

## Java
Java is a must have to set up a minecraft server, it's a condition we need to install first (remember to check if the java vers you install will work well with mc version you want on your server). For this tutorial we're using java 17. To install that we first should check if our system is updated well by:
```
sudo apt update
```

Then we can install the java itself. you can install it by typing:
```
sudo apt install openjdk-17-jdk
```

## Server setup
As mentioned earlier we'll do it on regular PC first, then just push it to our board with ssh.

1. **Download server pack of your choosing:** For the tutorial we'll be using Better minecraft mod https://www.curseforge.com/minecraft/modpacks/better-mc-forge-bmc4/files/7736926
2. **Edit your start up script:** We're talking about variables.txt file, which will be added as separate file to this repo. There's no too much to edit, but it's really important to do so. The thing we need to pay attention to is this line `JAVA_ARGS="-Xmx4G -Xms4G"`. It says how much ram your board should alocate to the sever. Xmx is max value, Xms is minimum. On our model we'll alocate `Xmx6G`, as minimum just set `Xms1G`. That's all. For other models of your board choose how much ram you want to alocate to your own likings, just remember that if you want to use your board at the moment the server is running, it's a lot easier to leave around 1 or 2 Gigs unalocated.

## SSH file transfer
For this you need to open a new powershell/terminal window. Then we can start by typing:
```
scp <path to your file PC> <board username>@<board ip adress>:<path where you want to have the files on your board>
```

And thst's it :)

## Unziping the files
Before we do it, we need to install thing called `unzip`, which will as it says unzip our .zip folder.
```
sudo apt install uznip
```

After we done that, we can actually uznip our file by:
```
unzip <name of the file>
```

## Starting server up
That's what we all've been waiting for, starting the server up. We do that by typing:
```
bash start.sh
```

It'll probably ask you to accept eula so just do it.
That's all! Enjoy your play guys

``Server is working on locale ip by now, if you want it worldwide, you can port it through playit.gg. Good luck 🫡``


