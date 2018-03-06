BitGold Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/bitbaba/bitgold.svg?branch=master)](https://travis-ci.org/bitbaba/bitgold)

Downloads
-------------

- [Win32](https://bintray.bitbaba.com/bitgold/bitgold-win32.tar.gz)
- [Ubuntu](https://bintray.bitbaba.com/bitgold/bitgold-ubuntu64.tar.gz)
- [Mac](https://bintray.bitbaba.com/bitgold/bitgold-mac.tar.gz)

Services
----------------

- [Pool](https://pool.bitbaba.com/)

- [Explorer](https://bitgold.bitbaba.com/)

- [Exchange](https://ex.bitbaba.com/)


What is BitGold?
----------------

BitGold is an new digital gold that enables instant payments to
anyone, anywhere in the world. BitGold uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. BitGold Core is the name of open source
software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the BitGold Core software, see https://bintray.bitbaba.com/bintray/bitgold, or read the
[bitgold design](http://blog.csdn.net/hacode/article/details/78369398) and
[bitcoin original whitepaper](https://bitcoincore.org/bitcoin.pdf).


License
-------

BitGold Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Features
--------

- 5 minutes per block(half of bitcoin core)
- 2-Mega-bytes serialized block size(2x bitcoin core)
- 42,000,000 coins(2x of bitcoins and half of litecoins)
- Seg-Witness(same as bitcoin core)
- sha256d as PoW (same as bitcoin core)

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitbaba/bitgold/tags) are created
regularly to indicate new official, stable release versions of BitGold Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://lists.linuxfoundation.org/mailman/listinfo/bitgold-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #bitgold-core-dev.


Automated Building
------------------

As you known, the .travis.yml is used for automated building. and here is a localized script called *travis.sh*, 
which can be used to build bitgold on your local laptop.

Example Usage:

```
mkdir -p depsrc; \
ln -s $PWD/depsrc depends/sources; \
sh travis.sh Win32Gui bitgold
```

>Note: *depsrc* is used to cache locale source tarballs of depends.


Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[BitGold Core's Transifex page](https://www.transifex.com/projects/p/bitgold/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Translators should also subscribe to the [mailing list](https://groups.google.com/forum/#!forum/bitgold-translators).
