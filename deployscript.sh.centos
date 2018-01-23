echo "Starting deployment script run"
sudo yum check-update
curl --silent --location https://rpm.nodesource.com/setup_8.x | sudo bash -
sudo yum install -y nodejs
sudo npm install
sudo yum install -y nginx
sudo rm -f /etc/nginx/conf.d/default.conf && sudo cp node-app-nginx-config /etc/nginx/conf.d/node-app-nginx-config.conf
sudo service nginx restart
sudo npm install -g pm2 && sudo pm2 start -f app.js
# sudo pm2 startup systemd && sudo pm2 save
echo "End of script run"
