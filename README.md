# docker-php
Docker compose to run PHP application, given Symfony configuration as an example.

[![Build Status](https://travis-ci.org/kariae/docker-php.svg?branch=master)](https://travis-ci.org/kariae/docker-php) ![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
## Installation
1. Create a `.env` from `.env.dist` file, and customize it according to your preferences.
2. Update your hosts file according to the [NGINX server configuration](https://github.com/kariae/docker-php/blob/master/nginx/conf.d/lekode.conf#L2)
```bash
# UNIX
sudo echo "0.0.0.0 lekode.dev" >> /etc/hosts
# Windows (edit C:\Windows\System32\drivers\etc\hosts)
```
3. Build containers
`docker-compose build`

## Usage
After building the containers, just run them and you’re ready to go
`docker-compose up -d`

## Utils
Here is a list of things that can help you

### xDebug
- [ ] TODO: How to configure xDebug with a code editor.

### Customize containers for different environment
- [ ] TODO: Add other useful containers (Redis, phpMyAdmin …)
- [ ] TODO: Customize NGINX for other frameworks than Symfony (Add .conf file per framework)

### Execute commands inside containers
You may need to execute commands inside php-fpm container to clear Symfony cache, install fixtures or whatever, to do this, check your container name from running containers list, connect to your container, and execute your command
```bash
docker ps
docker exec -ti lekode.lab.php sh
php bin/console ...
```

## Contributing
First, **many thanks** for your contributions, please note that this eco system is a personal preference that I use in most of my PHP projects (using Symfony or other frameworks), if you find any typo/misconfiguration, or just want to optimize more the workflow, please
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History
TODO: Write history

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/kariae/docker-php/blob/master/LICENSE) file for details
