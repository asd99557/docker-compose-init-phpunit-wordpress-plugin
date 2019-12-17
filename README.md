# Docker Compose init PHPUnit WordPress plugin

This project supplies environment to init WordPress plugin to start TDD.

[Plugin Unit Tests – WP-CLI — WordPress.org](https://make.wordpress.org/cli/handbook/plugin-unit-tests/#running-tests-on-travis-ci)

You can skip much steps to prepare environment to run WP-CLI.
And you will be able to get files for test with [few steps](#Quickstart).

## Requirement

- Docker
- Docker Compose

## Quickstart

#### 1. Clone or download

#### 2. Put test target plugin directory into "plugins" directory

#### 3. Enter directory and Docker Compose up (detach)

```shell script
cd docker-compose-init-phpunit-wordpress-plugin
docker-compose up -d
```

#### 4. Enter into wordpress container

```shell script
docker exec -it wordpress /bin/bash
```

#### 5. Init WordPress temporary

```shell script
wp --allow-root core install --url=localhost --title=temporary --admin_user=admin --admin_email=admin@localhost.com
```

#### 6. Generate files for test

```shell script
wp --allow-root scaffold plugin-tests (plugin directory name)
```

Then, you'll get files for test.

## References

- [Plugin Unit Tests – WP-CLI — WordPress.org](https://make.wordpress.org/cli/handbook/plugin-unit-tests/)
- [wordpress - Docker Hub](https://hub.docker.com/_/wordpress)
