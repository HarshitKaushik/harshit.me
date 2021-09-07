# harshit.me

Static website for harshit.me.

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
scp -r blog/public/*  root@157.245.101.248:/var/www/harshit.me/
```

Path of the main website.

```bash
/var/www/harshit.me/
```
