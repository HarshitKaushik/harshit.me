# harshit.me

Static website for uniharsh.com

## Commands

Install hugo server.

```bash
# on macOS
brew install hugo
# on debian/ubuntu
brew install hugo
# on windows
choco install hugo -confirm
```

Run hugo server.

```bash
hugo server
```

Compile hugo site.

```bash
hugo
```

Deploy the site to play-mine server.

```bash
scp -r blog/public/*  root@157.245.101.248:/var/www/uniharsh.com/
```

Path of the main website.

```bash
/var/www/uniharsh.com/
```

Set up the certificates for https using certbot.

```bash
# make sure that your version of snapd is up to date.
sudo snap install core; sudo snap refresh core
# if you have any Certbot packages installed using an OS package manager like apt, dnf, or yum, 
# you should remove them before installing the Certbot snap to ensure that when you run the command
# certbot the snap is used rather than the installation from your OS package manager
sudo apt-get remove certbot
# install certbot
sudo snap install --classic certbot
# run this command to get a certificate and have Certbot edit your nginx configuration automatically to serve it, turning on HTTPS access in a single step.
sudo certbot --nginx
# test automatic renewal
# the Certbot packages on your system come with a cron job or systemd timer that will renew your certificates automatically before they expire. You will not need to run Certbot again, unless you change your configuration.
# you can test automatic renewal for your certificates by running this command
sudo certbot renew --dry-run
```

Test nginx configuration and restart nginx service.

```bash
sudo nginx -t
sudo systemctl restart nginx
```