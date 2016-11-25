Team and repository tags
========================

[![Team and repository tags](http://governance.openstack.org/badges/deb-python-steadymark.svg)](http://governance.openstack.org/reference/tags/index.html)

<!-- Change things from this point on -->

# Steady Mark
> version 0.7.3
[![Build Status](https://secure.travis-ci.org/gabrielfalcao/steadymark.png?branch=master)](http://travis-ci.org/#!/gabrielfalcao/steadymark)
[![instanc.es Badge](https://instanc.es/bin/gabrielfalcao/steadymark.png)](http://instanc.es)
![meme](http://cdn.memegenerator.net/instances/400x/24908847.jpg)

# Turning your github readme files into python test suites since 2012

Steady Mark was created for python developers that love Github and
markdown.

## How it works:

Write your documentation using [github-flavored markdown](http://github.github.com/github-flavored-markdown/), surround your
snippets with python code blocks and steadymark will automatically
find and run them, if there is a header preceeding your python snippet
it will be used as title for your test.

# Advantages:

* Add test coverage to your app/library while documenting it
* Never have old malfunctional examples on your project's main page in github
* It uses [misaka](http://misaka.61924.nl/) which is a python-binding of [sundown](https://github.com/tanoku/sundown), the markdown engine that github uses in itself

# Example

## unicode.lower transforms string into lowercase

```python
from sure import expect
assert expect(u"Gabriel Falcao".lower()).equals(u"gabriel falcao")
```

## python can add numbers

```python
assert (2 + 2) == 4, 'oops baby'
```

# Start using steady mark now!

This is the code for the example above, copy and paste in you python
project right now and start keeping your documentation up-to-date with
the code.

    # My project name
    `version 0.1`

    ## unicode.lower transforms string into lowercase

    ```python
    assert "LOWERCaSe".lower() == "lowercase"
    ```

    ## python can add numbers

    ```python
    assert (2 + 2) == 5, 'oops baby'
    ```

Just run with:

```bash
$ steadymark README.md
```

## loading a python file before running tests

you can tell steadymark to load a "boot" file before running the tests, it's very useful for hooking up [sure](http://falcao.it/sure) or [HTTPretty](http://falcao.it/HTTPretty)


# Steadymark is on version 0.7.3

```python
>>> from sure import expect
>>> from steadymark import version
>>> assert expect(version).should.equal("0.7.3")
```
