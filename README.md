# netlink [![Build Status](https://travis-ci.org/mdlayher/netlink.svg?branch=master)](https://travis-ci.org/mdlayher/netlink) [![GoDoc](https://godoc.org/github.com/mdlayher/netlink?status.svg)](https://godoc.org/github.com/mdlayher/netlink) [![Go Report Card](https://goreportcard.com/badge/github.com/mdlayher/netlink)](https://goreportcard.com/report/github.com/mdlayher/netlink)

Package `netlink` provides low-level access to Linux netlink sockets.
MIT Licensed.

For more information about how netlink works, check out my blog series
on [Linux, Netlink, and Go](https://medium.com/@mdlayher/linux-netlink-and-go-part-1-netlink-4781aaeeaca8).

## Stability

At this time, package `netlink` is in a pre-v1.0.0 state. Changes are being made
which may impact the exported API of this package and others in its ecosystem.
To follow along on the status of a v1.0.0 release, [see the associated issue](https://github.com/mdlayher/netlink/issues/123).

**If you depend on this package in your applications, please vendor it or use Go
modules when building your application.**

## Design

A [number of netlink packages](https://godoc.org/?q=netlink) are already
available for Go, but I wasn't able to find one that aligned with what
I wanted in a netlink package:

- Straightforward, idiomatic API
- Well tested
- Well documented
- Doesn't use package/global variables or state
- Doesn't necessarily need root to work

My goal for this package is to use it as a building block for the creation
of other netlink family packages. For a list of these packages and others, see
[the importers list on godoc.org](https://godoc.org/github.com/mdlayher/netlink?importers).
