# Terminus Decoupled Kit Plugin

Currently a proof of concept.

## Installation

* Clone https://github.com/pantheon-systems/terminus-decoupled-kit-plugin
* `cd terminus-decoupled-kit-plugin`
* `composer install`
* `terminus self:plugin:install .`

## Usage

Run interactively:

```
terminus decoupled-kit:create
```

Run with command line flags:

```
terminus decoupled-kit:create my-site-name "My Site Label" --org="My Org" --cms=drupal --install-cms=FALSE
```

If you use the `--install-cms=FALSE` flag, the CMS sites won’t be installed automatically.
This allows you to install the site with your preferred options. `--install-cms` is an optional flag,
if it’s not provided, the default value is `TRUE`.


# Terminus Plugin Example

[![CircleCI](https://circleci.com/gh/pantheon-systems/terminus-plugin-example.svg?style=shield)](https://circleci.com/gh/pantheon-systems/terminus-plugin-example)
[![Actively Maintained](https://img.shields.io/badge/Pantheon-Actively_Maintained-yellow?logo=pantheon&color=FFDC28)](https://pantheon.io/docs/oss-support-levels#actively-maintained-support)

[![Terminus v2.x - v3.x Compatible](https://img.shields.io/badge/terminus-2.x%20--%203.x-green.svg)](https://github.com/pantheon-systems/terminus-plugin-example/tree/2.x)

A simple plugin for Terminus-CLI to demonstrate how to add new commands.

Adds commands 'hello' and 'auth:hello' to Terminus. Learn more about Terminus Plugins in the
[Terminus Plugins documentation](https://pantheon.io/docs/terminus/plugins)

## Configuration

These commands require no configuration

## Usage
* `terminus hello`
* `terminus auth:hello`

## Installation

To install this plugin using Terminus 3:
```
terminus self:plugin:install terminus-plugin-example
```

On older versions of Terminus:
```
mkdir -p ~/.terminus/plugins
curl https://github.com/pantheon-systems/terminus-plugin-example/archive/2.x.tar.gz -L | tar -C ~/.terminus/plugins -xvz
```

## Testing
This example project includes four testing targets:

* `composer lint`: Syntax-check all php source files.
* `composer cs`: Code-style check.
* `composer unit`: Run unit tests with phpunit
* `composer functional`: Run functional test with bats

To run all tests together, use `composer test`.

Note that prior to running the tests, you should first run:
* `composer install`
* `composer install-tools`

## Help
Run `terminus help auth:hello` for help.
