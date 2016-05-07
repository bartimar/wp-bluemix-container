# Docker WordPress migration image for IBM Bluemix
A Docker image for migrating your WordPress to IBM Bluemix Containers

## Fixes Bluemix permissions problem
Fixes Docker containers failing on bluemix due to nfs4 root->non-root translation on bluemix Volumes with chown.disabled (see Dockerfile)

## Migrate content
Migrate your previous wordpress from VPS to Bluemix by few simple commands (adjust as you need)

`git clone https://github.com/bartimar/wp-bluemix-container && cd wp-bluemix-container && tar cvzf content.tar.gz /var/www/wordpress/html/* && cf ic build -t wordpress .`

I find this way to get your content to IBM Bluemix volume the easiest, fastest and secure (it is not exposed publicly). It can be done several ways and this one is not perfect, don't hesitate to tell me a better way to do this. 
