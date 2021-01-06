# Francesca Woodman Theater Performance (work in progress)#

## software for audio LAN installation ##

### requirements ###
for midi input (so the server side)

`pip3 install mido`

for websockets to communicate to the radios in LAN (for the server and the clients)

`pip3 install websockets`

for playing the music files 

`pip3 install pygame`


after having installed the required python libraries you can run with

`python3 server.py` or `chmod +x` the file to make it executable.

The server will be listening to any incoming midi device that is connected (before boot). It will then broadcast certain commands depending on the incoming midi msg through websockets.

`python3 client.py` will launch a client that receives the command via websockets


## troubleshooting ## 

#### the clients are not connecting to the server? ####
  - Make sure the ip settings in the config.ini file is that of the machine running the server
  - Make sure the server has no firewall blocking the connections 
