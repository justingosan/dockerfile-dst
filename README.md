# Dont Starve Together Dedicated Server Docker Container

1. Install docker and clone this repo somewhere
2. Modify **settings.ini** and **server_token.txt** [Link](http://dont-starve-game.wikia.com/wiki/Guides/Don%E2%80%99t_Starve_Together_Dedicated_Servers)
3. Choose a <host_volume> to put persistent files e.g `mkdir /docker/dst`
4. Make default DoNotStarveTogether directory in host volume `mkdir /docker/dst/DoNotStarveTogether`
5. Copy  **settings.ini** and **server_token.txt** to <host_volume>/DoNotStarveTogether `cp settings.ini server_token.txt /docker/dst/DoNotStarveTogether`
6. Run `docker build -t dst .`
7. Run `docker run -d -p 10999:10999/udp -v /docker/dst:/data dst`