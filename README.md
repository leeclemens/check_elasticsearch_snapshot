# check_elasticsearch_snapshot

[![Master Build Status](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot.svg?branch=master)](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot)
[![Develop Build Status](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot.svg?branch=develop)](https://travis-ci.org/leeclemens/check_elasticsearch_snapshot)

Check Elasticsearch Snapshot

A basic Nagios/Icinga plugin to check the status and age of an Elasticsearch snapshot.

By default all Snapshots are checked for status and age. You can also specify a specific repository to check.

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
```bash
./check_elasticsearch_snapshot --help
```

`[-h] -s SERVER -p PORT -w WARNING -c CRITICAL [-r REPOSITORY]`

### Thresholds
The following suffixes can be used; an entirely numeric value is considered as milliseconds.
* s - seconds
* m - minutes
* h - hours
* d - days
* w - weeks
#### Threshold Examples
* `3h` is 3 hours
* `1.25d` is 1 day and 6 hours

### Examples
```bash
check_elasticsearch_snapshot -s localhost -p 9200 -w 1.1d -c 2d 
```
```bash
check_elasticsearch_snapshot -s localhost -p 9200 -w 2.1d -c 7.5d -r my_backups 
```

## Contributing
1. Fork the repo
2. Create a new feature branch
3. Make your edits, commit and push
4. Create a [Pull Request](https://github.com/leeclemens/check_elasticsearch_snapshot/pulls) against the develop branch

Or create an [Issue](https://github.com/leeclemens/check_elasticsearch_snapshot/issues) to report a bug or feature request
