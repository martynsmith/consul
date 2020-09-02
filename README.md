你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Consul [![Build Status](https://travis-ci.org/hashicorp/consul.png)](https://travis-ci.org/hashicorp/consul)

* Website: https://www.consul.io
* IRC: `#consul` on Freenode
* Mailing list: [Google Groups](https://groups.google.com/group/consul-tool/)

Consul is a tool for service discovery and configuration. Consul is
distributed, highly available, and extremely scalable.

Consul provides several key features:

* **Service Discovery** - Consul makes it simple for services to register
  themselves and to discover other services via a DNS or HTTP interface.
  External services such as SaaS providers can be registered as well.

* **Health Checking** - Health Checking enables Consul to quickly alert
  operators about any issues in a cluster. The integration with service
  discovery prevents routing traffic to unhealthy hosts and enables service
  level circuit breakers.

* **Key/Value Storage** - A flexible key/value store enables storing
  dynamic configuration, feature flagging, coordination, leader election and
  more. The simple HTTP API makes it easy to use anywhere.

* **Multi-Datacenter** - Consul is built to be datacenter aware, and can
  support any number of regions without complex configuration.

Consul runs on Linux, Mac OS X, and Windows. It is recommended to run the
Consul servers only on Linux, however.

## Quick Start

An extensive quick quick start is viewable on the Consul website:

https://www.consul.io/intro/getting-started/install.html

## Documentation

Full, comprehensive documentation is viewable on the Consul website:

https://www.consul.io/docs

## Developing Consul

If you wish to work on Consul itself, you'll first need [Go](https://golang.org)
installed (version 1.5.3+ is _required_). Make sure you have Go properly installed,
including setting up your [GOPATH](https://golang.org/doc/code.html#GOPATH).

Next, clone this repository into `$GOPATH/src/github.com/hashicorp/consul` and
then just type `make`. In a few moments, you'll have a working `consul` executable:

```
$ go get -u ./...
$ make
...
$ bin/consul
...
```

*note: `make` will also place a copy of the binary in the first part of your $GOPATH*

You can run tests by typing `make test`.

If you make any changes to the code, run `make format` in order to automatically
format the code according to Go standards.

### Building Consul on Windows

Make sure Go 1.5.3+ is installed on your system and that the Go command is in your
%PATH%.

For building Consul on Windows, you also need to have MinGW installed.
[TDM-GCC](http://tdm-gcc.tdragon.net/) is a simple bundle installer which has all
the required tools for building Consul with MinGW.

Install TDM-GCC and make sure it has been added to your %PATH%.

If all goes well, you should be able to build Consul by running `make.bat` from a
command prompt.

See also [golang/winstrap](https://github.com/golang/winstrap) and
[golang/wiki/WindowsBuild](https://github.com/golang/go/wiki/WindowsBuild)
for more information of how to set up a general Go build environment on Windows
with MinGW.

