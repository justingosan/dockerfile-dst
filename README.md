# Dont Starve Together Dedicated Server Docker Container

1. Install docker
2. Modify **settings.ini** and **server_token.txt** [Link](http://dont-starve-game.wikia.com/wiki/Guides/Don%E2%80%99t_Starve_Together_Dedicated_Servers)
3. Run `docker build -t dst .`
4. Run `docker run -d -p 10999:10999/udp -v <host_volume>:/data dst`