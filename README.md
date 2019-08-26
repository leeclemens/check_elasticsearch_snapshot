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
* `WARNING 3600` is 1 hour
* `WARNING 1d` is 1 day
* `WARNING 1.25d` is 1 day and 6 hours

### Examples
```bash
check_elasticsearch_snapshot -s localhost -p 9200 -w 1.1d -c 2d 
```
```bash
check_elasticsearch_snapshot -s localhost -p 9200 -w 2.1d -c 7.5d -r my_backups 
```

## Contributing
1. Fork the repo
  * Create a new feature branch
2. Make your edits, commit and push
3. Create a [Pull Request](https://github.com/leeclemens/check_elasticsearch_snapshot/pulls)

Or just create an [Issue](https://github.com/leeclemens/check_elasticsearch_snapshot/issues) to report a bug or feature request
