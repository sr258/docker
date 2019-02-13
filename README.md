# Weblate image for Docker

[![Build Status](https://travis-ci.org/WeblateOrg/docker.svg?branch=master)](https://travis-ci.org/WeblateOrg/docker)
[![Docker Layers](https://images.microbadger.com/badges/image/weblate/weblate.svg)](https://microbadger.com/images/weblate/weblate "Get your own image badge on microbadger.com")
[![Requirements Status](https://requires.io/github/WeblateOrg/docker/requirements.svg?branch=master)](https://requires.io/github/WeblateOrg/docker/requirements/?branch=master)

Docker container for Weblate

You might want to use [Weblate docker-compose](https://github.com/WeblateOrg/docker-compose) to run Weblate.

## sr258's fork

This fork is makes the Weblate Docker container compatible with H5P and GitHub

* It changes the JSON formatter to output correctly nested JSON (for simplicity's sake if you just select JSON)
* It allows you to add the GitHub OAuth token as an environment variable (WEBLATE_GITHUB_OAUTH_TOKEN)
* It fixes issues with access rights to ~/.config/hub (changes location to /home/weblate/.config/hub and automatically creates the file with the token from WEBLATE_GITHUB_OAUTH_TOKEN)

## Docker hub tags

You can use following tags on Docker hub:

* `latest` - latest stable release
* `edge` - bleeding edge docker image (contains stable Weblate, but the Docker image changes might not yet be fully tested)
* specific tag from [weblate/weblate](https://hub.docker.com/r/weblate/weblate/tags/) image

## Documentation

Detailed documentation is available in Weblate documentation:

https://docs.weblate.org/en/latest/admin/deployments.html#docker
