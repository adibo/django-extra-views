Change History
==============

0.10.0 (2018-02-28)
------------------
Supported Versions:

========== ==========
python     Django
========== ==========
2.7        1.7 - 1.11
3.4 - 3.6  1.8 - 1.11
========== ==========

New features:

- Added SuccessMessageWithInlinesMixin (#151)
- Allow the formset prefix to be overrideen (#154)

Bug fixes:

- SearchableMixin: Fix reduce() of empty sequence error (#149)
- Add fields attributes (Issue #144, PR #150)
- Fix Django 1.11 AttributeError: This QueryDict instance is immutable (#156)

0.9.0 (2017-03-08)
------------------
This version supports Django 1.7, 1.8, 1.9, 1.10 (latest minor versions), and Python 2.7, 3.4, 3.5 (latest minor versions).

- Added Django 1.10 support 
- Dropped Django 1.6 support

0.8 (2016-06-14)
----------------

This version supports Django 1.6, 1.7, 1.8, 1.9 (latest minor versions), and Python 2.7, 3.4, 3.5 (latest minor versions).

- Added ``widgets`` attribute setting; allow to change form widgets in the ``ModelFormSetView``.
- Added Django 1.9 support.
- Fixed ``get_context_data()`` usage of ``*args, **kwargs``.
- Fixed silent overwriting of ``ModelForm`` fields to ``__all__``.


Backwards-incompatible changes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Dropped support for Django <= 1.5 and Python 3.3.
- Removed the ``extra_views.multi`` module as it had neither documentation nor
  test coverage and was broken for some of the supported Django/Python versions.
- This package no longer implicitly set ``fields = '__all__'``.
  If you face ``ImproperlyConfigured`` exceptions, you should have a look at the
  `Django 1.6 release notes`_ and set the ``fields`` or ``exclude`` attributes
  on your ``ModelForm`` or extra-views views.

.. _Django 1.6 release notes: https://docs.djangoproject.com/en/stable/releases/1.6/#modelform-without-fields-or-exclude


0.7.1 (2015-06-15)
------------------
Begin of this changelog.
