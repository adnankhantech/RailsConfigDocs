##Install Passenger
```
gem install passenger
rvmsudo passenger-install-nginx-module
```

##Change Nginx Conf
```
sudo nano /opt/nginx/conf/nginx.conf
```

## Nginx Startup Setup
```
mkdir software
cd software
git clone git://github.com/jnstq/rails-nginx-passenger-ubuntu.git
sudo mv rails-nginx-passenger-ubuntu/nginx/nginx /etc/init.d/nginx
sudo ln -s /etc/init.d/nginx /usr/local/bin/nginx
sudo update-rc.d nginx defaults
```

## Nginx Configuration to setup new rails application
```
nginx.conf file

server {
    listen 80;
    server_name www.project.com;
    root /home/user/project_name/public;
    passenger_enabled on;
    rails_env development;
    }
```