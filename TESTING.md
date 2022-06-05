Testing the Code
=====
This is just a generalized placeholder for "how do we best test this
monster." Documentation is currently what's here... at least until we
get a better handle on "how" to best test it.


# Premise and  Resources

One of the early things needs to be reproducible unittest, doctest, and
similar. Moat-likely, this will all end up under `tox`, but this
document should help put together overall resources until a firm path
and/or template is determined.


## Testing Frameworks

* Built-In
** [doctest](https://docs.python.org/3/library/doctest.html)
** [unittest](https://docs.python.org/3/library/unittest.html)
* Modules
* [nose](https://nose.readthedocs.io/en/latest/)
* [PyTest](https://docs.pytest.org/en/latest/)
** [plugins](https://docs.pytest.org/en/latest/reference/plugin_list.html)
** [pytest-nose](https://docs.pytest.org/en/latest/how-to/nose.html)
** [pytest-unittest](https://docs.pytest.org/en/latest/how-to/unittest.html)

### Testing Python Argument/blogs/diatribes:

* https://docs.python-guide.org/writing/tests/
* https://python.plainenglish.io/writing-good-unit-tests-in-python-with-ease-5fb6d7aa2b77

### Other Python Testing Tools

* [Hypothesis](https://hypothesis.readthedocs.io/en/latest/)
* [Taxonomy](https://wiki.python.org/moin/PythonTestingToolsTaxonomy)
* [tox](https://tox.wiki/en/latest/)
