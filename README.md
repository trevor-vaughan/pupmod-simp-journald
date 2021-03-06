[![License](https://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/73/badge)](https://bestpractices.coreinfrastructure.org/projects/73)
[![Puppet Forge](https://img.shields.io/puppetforge/v/simp/journald.svg)](https://forge.puppetlabs.com/simp/journald)
[![Puppet Forge Downloads](https://img.shields.io/puppetforge/dt/simp/journald.svg)](https://forge.puppetlabs.com/simp/journald)
[![Build Status](https://travis-ci.org/simp/pupmod-simp-journald.svg)](https://travis-ci.org/simp/pupmod-simp-journald)

#### Table of Contents

1. [Overview](#overview)
2. [Setup - The basics of getting started with journald](#setup)
    * [Setup requirements](#setup-requirements)
    * [Beginning with journald](#beginning-with-journald)
3. [Limitations - OS compatibility, etc.](#limitations)
4. [Development - Guide for contributing to the module](#development)

## Overview

systemd-journald is a system service that collects and stores logging data. 
It creates and maintains structured, indexed journals based on logging information 
that is received from a variety of sources:

* Kernel log messages, via kmsg
* Simple system log messages, via the libc syslog(3) call
* Structured system log messages via the native Journal API, see sd_journal_print(4)
* Standard output and standard error of system services
* Audit records, via the audit subsystem

## Setup

### Beginning with journald

    include journald

## Usage

    class {'journald': options => {
	    'Compress'          => 'yes',
	    'ForwardToSyslog'   => 'yes',
	    'ForwardToKMsg'     => 'yes',
	    'ForwardToConsole'  => 'no',
	    'TTYPath'           => '/dev/console',
	  }
    }

## Limitations

This module is only appicable on EL7 machines

## Development

* Fork the project
* Commit and push until you are happy with your contribution
* Send a pull request with a description of your changes
