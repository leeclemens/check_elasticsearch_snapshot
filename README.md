# check_elasticsearch_snapshot

[![Master Build Status](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot.svg?branch=master)](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot)
[![Develop Build Status](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot.svg?branch=develop)](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot)

Check Elasticsearch Snapshot

A basic Nagios/Icinga plugin to check the status and age of an Elasticsearch snapshot.

By default all Snapshots are checked for status and age. You can also specify a specific snapshot to check.

## Installation
### Requirements
* Python 3.4+
* Python requests package
  * pip install requests
  * RedHat/CentOS
    * python34-requests.noarch
      * -or-
    * python36-requests.noarch
### Plugin Installation
* Download check_elasticsearch_snapshot to your PluginContribDir
* Add/Import the CheckCommand configuration

## Usage

./check_elasticsearch_snapshot --help

## Contributing
1. Fork the repo
  * Create a new feature branch
2. Make your edits, commit and push
3. Create a [Pull Request](https://github.com/leeclemens/check_elasticsearch_snapshot/pulls)

Or just create an [Issue](https://github.com/leeclemens/check_elasticsearch_snapshot/issues) to report a bug or feature request
