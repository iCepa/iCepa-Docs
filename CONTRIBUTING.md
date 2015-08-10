# Contributing

## Code Style

* Prefer memory-safe code and languages (Swift, Rust)
* [Swift Style Guide](https://github.com/github/swift-style-guide)
* [Objective-C Style Guide](https://github.com/github/objective-c-style-guide)
* [Rust Style Guide](http://aturon.github.io/README.html)

## Releases

* All releases will be versioned according to [semver](http://semver.org)
* All release tags must be [signed](https://git-scm.com/book/tr/v2/Git-Tools-Signing-Your-Work)
* Signing each commit may be overkill

## Code Review

* Every feature/bugfix/etc should be done in a feature branch.
* To merge into master, submit a PR on GitHub to allow for code review.
* Ideally before merging, it should be reviewed by at least 1 other person.

## Tests

* All code should be written in a way that [facilitates testing](http://programmers.stackexchange.com/questions/153410/what-are-the-design-principles-that-promote-testable-code-designing-testable-c)
* New code should be accompanied by unit tests and integration tests
* TDD (test driven development) is very helpful for quick iteration

## Dependencies

* 3rd party dependencies should be minimized if possible
* Prefer Cocoapods or Carthage over submodules

## License

* By contributing you affirm you have the rights to all the code you provide
* All code should be permissively licensed
* We should use the [Tor LICENSE](https://gitweb.torproject.org/tor.git/plain/LICENSE)
