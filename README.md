# Official Docker container for Weblate

[![Build Status](https://travis-ci.com/WeblateOrg/docker.svg?branch=master)](https://travis-ci.com/WeblateOrg/docker)
[![Docker Layers](https://images.microbadger.com/badges/image/weblate/weblate.svg)](https://microbadger.com/images/weblate/weblate "Get your own image badge on microbadger.com")
[![Documenation](https://img.shields.io/readthedocs/weblate.svg)](https://docs.weblate.org/en/latest/admin/install/docker.html)

Weblate is a libre software web-based continuous localization system used by
over 1150+ opensource projects & companies in over 115+ countries around the
World.

You might want to use [Weblate docker-compose](https://github.com/WeblateOrg/docker-compose) to run Weblate.

## sr258's fork

This fork is makes the Weblate Docker container compatible with H5P and GitHub

* It changes the JSON formatter to output correctly nested JSON (for simplicity's sake if you just select JSON)
* It allows you to add the GitHub OAuth token as an environment variable (WEBLATE_GITHUB_OAUTH_TOKEN)
* It fixes issues with access rights to ~/.config/hub (changes location to /home/weblate/.config/hub and automatically creates the file with the token from WEBLATE_GITHUB_OAUTH_TOKEN)

## Exposed ports

In July 2019 (starting with the 3.7.1-6 tag), the containers is not running as
root. As a consequence this has lead to changed exposed port from 80 to 8080.

## Docker hub tags

You can use following tags on Docker hub:

* `latest` - latest stable release
* `edge` - bleeding edge docker image (contains stable Weblate, but the Docker image changes might not yet be fully tested)
* specific tag from [weblate/weblate](https://hub.docker.com/r/weblate/weblate/tags/) image

## Documentation

Detailed documentation is available in Weblate documentation:

https://docs.weblate.org/en/latest/admin/install/docker.html
