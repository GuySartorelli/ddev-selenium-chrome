[![tests](https://github.com/drud/ddev-redis/actions/workflows/tests.yml/badge.svg)](https://github.com/drud/ddev-redis/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2022.svg)

## What is this?

This repository allows you to quickly add [selenium standalone chrome](https://github.com/SeleniumHQ/docker-selenium) to a [Ddev](https://ddev.readthedocs.io) project.

## Installation

For DDEV v1.23.5 or above run

```sh
ddev add-on get thunder/ddev-selenium-chrome
```

For earlier versions of DDEV run

```sh
ddev get thunder/ddev-selenium-chrome
```

Then restart your project

```sh
ddev restart
```

## Explanation

This selenium standalone chrome recipe for [ddev](https://ddev.readthedocs.io) installs a [`.ddev/docker-compose.selenium.yaml`](docker-compose.selenium.yaml) using the `selenium/standalone-chrome:latest` docker image.

## Interacting with Selenium standalone chrome

* The selenium chrome instance will listen on TCP port 4444.
* For debugging use `selenium/standalone-chrome-debug:latest` image and add port mapping for vnc, reachable at `vnc://localhost:6000`, if you get a prompt asking for a password, it is: `secret`.

