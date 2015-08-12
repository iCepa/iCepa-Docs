# iCepa-Docs
Documentation scratchpad for iOS Tor VPN implementation. Below are the different components that we'll probably need.

## Style Guide

* Check out [CONTRIBUTING.md](https://github.com/iCepa/iCepa-Docs/blob/master/CONTRIBUTING.md)
* Signing git commits
* Pull request code review process
* Test coverage
* LICENSE (permissive / same as [Tor](https://gitweb.torproject.org/tor.git/plain/LICENSE))
* Writing memory-safe code

## Tor.framework

* Wrap Tor binary
* Wrap control port
* Standalone iOS 8 framework
* Separate repo
* [Tor Control Port](https://gitweb.torproject.org/torspec.git/tree/control-spec.txt)
* [Tor Manual](https://www.torproject.org/docs/tor-manual.html.en)

## TorPacketTunnelProvider

* Separate repo
* Integrates Tor.framework
* NEPacketTunnelProvider
* Integrates tun2socks
* Prevent information leaks via domain/IP whitelist

## tun2socks

* Separate repo
* Convert [Conrad's Notes](https://docs.google.com/document/d/1ob96eK-qjrxzIdNEmglClaH3kI-O5CfT9tp1xnXwksc/edit?usp=sharing) to README.md
* [tun2socks-iOS](https://github.com/shadowsocks/tun2socks-iOS) - Currently Empty
* [tun2socks-iOS](https://github.com/linusyang/tun2socks-iOS) - [@linusyang](https://github.com/linusyang) branch
* [tun2socks](https://github.com/ambrop72/badvpn/tree/master/tun2socks) - Upstream tun2socks repo
* [lwIP](http://savannah.nongnu.org/projects/lwip/) - Lightweight TCP/IP stack written in C

#### tun2socks-rust

* Rewrite this as resuable Rust crate for memory safety and portability?
* Write Obj-C or Swift wrapper for exported Rust C API

## Tor for iOS App UI

* Get designer(s)
* Keep It Simple
* Prevent users from accidentally leaking information
* Get feedback from designers on how to implement on-demand whitelist
* Sketch out some storyboards (use iOS Storyboards?)
* OS X support (???)

# Helpful Links

## NETunnelProviderManager

* [Class reference](https://developer.apple.com/library/prerelease/ios/documentation/NetworkExtension/Reference/NETunnelProviderManagerClassRef/index.html#//apple_ref/doc/uid/TP40016295)
* [WWDC Session about Network Extensions](https://developer.apple.com/videos/wwdc/2015/?id=717)
* [Sample code: SimpleTunnel](https://github.com/ios-sample-code/SimpleTunnel)
* [ShadowVPN-iOS](https://github.com/clowwindy/ShadowVPN-iOS) - Includes Swift PacketTunnelProvider Example 
* [shadowsocks-iOS](https://github.com/shadowsocks/shadowsocks-iOS/issues/124) - Issue 124: "Adopting iOS 9 network extension points" discussion thread

## Secure Coding

* [Apple Secure Coding Guide](https://developer.apple.com/library/mac/documentation/Security/Conceptual/SecureCodingGuide/Introduction.html)
* [Swift Style Guide](https://github.com/github/swift-style-guide)
* [Objective-C Style Guide](https://github.com/github/objective-c-style-guide)
* [Rust Style Guide](http://aturon.github.io/README.html)

## Tor

* [Tor Control Port](https://gitweb.torproject.org/torspec.git/tree/control-spec.txt)
* [Tor Manual](https://www.torproject.org/docs/tor-manual.html.en)

## Rust

#### Learning Rust

* [Rust in Detail: Writing Scalable Chat Service from Scratch](https://nbaksalyar.github.io/2015/07/10/writing-chat-in-rust.html)
* [Rust Once, Run Everywhere](http://blog.rust-lang.org/2015/04/24/Rust-Once-Run-Everywhere.html) (Rust/C FFI)
* [Rust Style Guide](http://aturon.github.io/README.html)

#### Rust IDE

* [Atom](https://atom.io) and [Sublime](https://www.sublimetext.com) both have Rust language plugins
* [racer](https://github.com/phildawes/racer) - Rust autocomplete
