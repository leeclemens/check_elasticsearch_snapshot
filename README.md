# Check Elasticsearch Snapshot

[![License](https://img.shields.io/github/license/leeclemens/check_elasticsearch_snapshot?style=for-the-badge)](https://github.com/leeclemens/check_elasticsearch_snapshot/blob/master/LICENSE)
[![Current Version](https://img.shields.io/github/v/tag/leeclemens/check_elasticsearch_snapshot?style=for-the-badge)](https://github.com/leeclemens/check_elasticsearch_snapshot/tags)
[![Issues](https://img.shields.io/github/issues-raw/leeclemens/check_elasticsearch_snapshot?style=for-the-badge)](https://github.com/leeclemens/check_elasticsearch_snapshot/issues?q=is%3Aopen+is%3Aissue)
[![Pull Requests](https://img.shields.io/github/issues-pr-raw/leeclemens/check_elasticsearch_snapshot?style=for-the-badge)](https://github.com/leeclemens/check_elasticsearch_snapshot/pulls?q=is%3Aopen+is%3Apr)

[![Master Build Status](https://img.shields.io/travis/com/leeclemens/check_elasticsearch_snapshot/master?style=for-the-badge&label=master:build)](https://app.travis-ci.com/github/leeclemens/check_elasticsearch_snapshot)
[![Master Codacy](https://img.shields.io/codacy/grade/b6015d104d834369a7f8cd8ae9679dc8/master?style=for-the-badge&label=master:code%20quality)](https://app.codacy.com/gh/leeclemens/check_elasticsearch_snapshot/dashboard?branch=master)

[![Develop Build Status](https://img.shields.io/travis/com/leeclemens/check_elasticsearch_snapshot/develop?style=for-the-badge&label=develop:build)](https://app.travis-ci.com/github/leeclemens/check_elasticsearch_snapshot)
[![Develop Codacy](https://img.shields.io/codacy/grade/b6015d104d834369a7f8cd8ae9679dc8/develop?style=for-the-badge&label=develop:code%20quality)](https://app.codacy.com/gh/leeclemens/check_elasticsearch_snapshot/dashboard?branch=develop)

## Description

A basic Nagios/Icinga plugin to check the status and age of an Elasticsearch snapshot.

By default, all Snapshots are checked for status and age.
You can also specify a specific repository to check.

## Installation

### Requirements

* Python 3.6+
* Python requests package
  * pip install requests
  * RedHat/CentOS
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
4. Create a [Pull Request](https://github.com/leeclemens/check_elasticsearch_snapshot/pulls)
against the develop branch

Or create an [Issue](https://github.com/leeclemens/check_elasticsearch_snapshot/issues)
to report a bug or feature
request
