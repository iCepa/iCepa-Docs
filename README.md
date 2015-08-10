# iCepa-Docs
Documentation scratchpad for iOS Tor VPN implementation. Below are the different components that we'll probably need.

## Style Guide

* Check out [CONTRIBUTING.md](https://github.com/iCepa/iCepa-Docs/blob/master/CONTRIBUTING.md)

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
* Integrates tun2socks-rust
* Prevent information leaks via domain/IP whitelist

### tun2socks-rust

* Separate repo
* Write this as resuable Rust crate for memory safety and portability?
* Write Obj-C or Swift wrapper for exported Rust C API
* Convert [Conrad's Notes](https://docs.google.com/document/d/1ob96eK-qjrxzIdNEmglClaH3kI-O5CfT9tp1xnXwksc/edit?usp=sharing) to README.md

## Tor for iOS App UI

* Get designer(s)
* Keep It Simple
* Prevent users from accidentally leaking information
* Get feedback from designers on how to implement on-demand whitelist
* Sketch out some storyboards (use iOS Storyboards?)
* OS X support (???)

# Helpful Links

## Secure Coding

* [Apple Secure Coding Guide](https://developer.apple.com/library/mac/documentation/Security/Conceptual/SecureCodingGuide/Introduction.html)

## Tor

* [Tor Control Port](https://gitweb.torproject.org/torspec.git/tree/control-spec.txt)
* [Tor Manual](https://www.torproject.org/docs/tor-manual.html.en)

## Learning Rust

* [Rust in Detail: Writing Scalable Chat Service from Scratch](https://nbaksalyar.github.io/2015/07/10/writing-chat-in-rust.html)
* [Rust Once, Run Everywhere](http://blog.rust-lang.org/2015/04/24/Rust-Once-Run-Everywhere.html) (Rust/C FFI)

#### Rust IDE

* [Atom](https://atom.io) and [Sublime](https://www.sublimetext.com) both have Rust language plugins
* [racer](https://github.com/phildawes/racer) - Rust autocomplete
