# Edward

[![Build Status](https://travis-ci.org/yext/edward.svg?branch=master)](https://travis-ci.org/yext/edward)
[![Go Report Card](https://goreportcard.com/badge/github.com/yext/edward)](https://goreportcard.com/report/github.com/yext/edward)

A command line tool for managing local instances of microservices.

Full documentation available at [http://engblog.yext.com/edward/](http://engblog.yext.com/edward/).

## Table of Contents  

* [Features](#features)
  * [Start multiple services with one command](#start-multiple-services-with-one-command)
  * [See status for running services](#see-status-for-running-services)
  * [Follow service logs](#follow-service-logs)
  * [Restart as needed](#restart-as-needed)
  * [Auto-restart on edits](#auto-restart-on-edits)
  * [Generate configuration automatically](#generate-configuration-automatically)
* [Installation](#installation)  
* [Updating](#updating)

## Features

### Start multiple services with one command

No need to start each service in its own terminal tab, just run `edward start` to build and launch multiple
services in the background!

![Starting services](images/start.gif)

### See status for running services

Run `edward status` to see which of your services are up and running, how long for, and on which ports
they are listening.

![View Status](images/status.gif)

### Follow service logs

Follow stdout and stderr for one or more services with `edward tail`.

![Follow logs](images/tail.gif)

### Restart as needed

Made some changes? Run `edward restart` to re-build and re-launch a service.

![Restart services](images/restart.gif)

### Auto-restart on edits

Edward will even automatically restart services when source files are changed.

![Auto-restart when files are edited](images/autorestart.gif)

### Generate configuration automatically

New services? Run `edward generate` to create a config file automatically.

![Generate configuration](images/generate.gif)

Edward can generate configuration for projects using:

* Go
* Docker
* ICBM
* Procfiles

Don't see your project described above? No problem! Edward can be manually configured for any
service that can be built and started from the command line.

## Installation

Edward uses the vendor folder, and as such, Go 1.6 is required.

    go get github.com/yext/edward

## Updating

To update an existing install to the latest version of Edward, run:

    go get -u github.com/yext/edward
