# go-curl

[![GoDoc Widget]][GoDoc]
[![Build Status](https://travis-ci.org/030/go-curl.svg?branch=master)](https://travis-ci.org/030/go-curl)
[![Go Report Card](https://goreportcard.com/badge/github.com/030/go-curl)](https://goreportcard.com/report/github.com/030/go-curl)
![Docker Pulls](https://img.shields.io/docker/pulls/utrecht/go-curl.svg)
![Issues](https://img.shields.io/github/issues-raw/030/go-curl.svg)
![Pull requests](https://img.shields.io/github/issues-pr-raw/030/go-curl.svg)
![Total downloads](https://img.shields.io/github/downloads/030/go-curl/total.svg)
![License](https://img.shields.io/github/license/030/go-curl.svg)
![Repository Size](https://img.shields.io/github/repo-size/030/go-curl.svg)
![Contributors](https://img.shields.io/github/contributors/030/go-curl.svg)
![Commit activity](https://img.shields.io/github/commit-activity/m/030/go-curl.svg)
![Last commit](https://img.shields.io/github/last-commit/030/go-curl.svg)
![Release date](https://img.shields.io/github/release-date/030/go-curl.svg)
![Latest Production Release Version](https://img.shields.io/github/release/030/go-curl.svg)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=bugs)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=code_smells)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=coverage)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=duplicated_lines_density)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=ncloc)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=alert_status)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=security_rating)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=sqale_index)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=030_go-curl&metric=vulnerabilities)](https://sonarcloud.io/dashboard?id=030_go-curl)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2845/badge)](https://bestpractices.coreinfrastructure.org/projects/2845)
[![codecov](https://codecov.io/gh/030/go-curl/branch/master/graph/badge.svg)](https://codecov.io/gh/030/go-curl)
[![BCH compliance](https://bettercodehub.com/edge/badge/030/go-curl?branch=master)](https://bettercodehub.com/results/030/go-curl)

## Usage

If one would like to upload a file, then the '@' character should be used like
in curl (see [Testing paragraph](#testing)):

```
./go-curl -url \
    http://localhost:9999/service/rest/v1/components?repository=maven-releases \
    -user admin -pass admin123 -F \
    "maven2.asset1=@utils/test-files-multipart/file1.pom,\
    maven2.asset1.extension=pom,\
    maven2.asset2=@utils/test-files-multipart/file1.jar,\
    maven2.asset2.extension=jar,\
    maven2.asset3=@utils/test-files-multipart/file1-sources.jar,\
    maven2.asset3.extension=sources.jar"
```

## Testing

### Integration

```
./integration-tests.sh
```

[GoDoc]: https://godoc.org/github.com/030/go-curl
[GoDoc Widget]: https://godoc.org/github.com/030/go-curl?status.svg
