# authors_api
searching authors

# Authors API Search

This project allows users to search for authors using the Open Library API. It is a simple web application that provides a user-friendly interface to search for authors by name and view their details, including work count and top work.

## Features
- Search for authors by name
- Display the number of works by the author
- Display the top work of the author (if available)
- Simple and intuitive UI

## Technologies Used
- HTML
- CSS
- JavaScript
- Open Library API (https://openlibrary.org/)

## Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/authors_api.git
   cd authors_api
   or scp -r repository ubuntu@web-01 or web-02:/home/ubuntu/ 
  ## giving credit
credit to the author and to the Open Library API for providing the data.
Great thanks to J. K. Rowling for creating this api
Open Library API (https://openlibrary.org/)
#vid 
https://youtu.be/dpRs7k6lEVw

**#author of this README.md**

Rachel Toronga

**Deploying**
Ubuntu servers (Web01, Web02, Lb01)
SSH access to all servers
Git installed on all servers
**Deploy** to Web01 & Web02
**Connect to Web01**
ssh username@web01_ip ssh username@web02_ip

**Update system and install Nginx**
sudo apt update && sudo apt upgrade -y sudo apt install nginx git -y

**Add the files in the web servers**
cd /var/www/html sudo vim index.html sudo vim styles.css sudo vim script.js sudo chown -R www-data:www-data /var/www/html

**Configure Nginx**
sudo nano /etc/nginx/sites-available/default

**Deploy on Lb01**
sudo apt update sudo apt install haproxy -y sudo nano /etc/haproxy/haproxy.cfg

**Configure HAProxy**
frontend http_front bind *:80 default_backend http_back

backend http_back balance roundrobin server web01_ip:80 check
server web02_ip:80 check

**HAProxy Status**
sudo systemctl status haproxy

**Open in browser**
open web01_ip address
