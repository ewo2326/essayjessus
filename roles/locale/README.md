Locale
======

This role helps to install and configure locale.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    locale_lang: en_US.UTF-8
    locale_language: en_US:en
    locale_generate:
      - "en_US.UTF-8 UTF-8"
      - "ru_RU ISO-8859-5"
      - "ru_RU.CP1251 CP1251"
      - "ru_RU.KOI8-R KOI8-R"
      - "ru_RU.UTF-8 UTF-8"
      - "ru_UA KOI8-U"
      - "ru_UA.UTF-8 UTF-8"
      - "uk_UA KOI8-U"
      - "uk_UA.UTF-8 UTF-8"

Variables 'locale_lang', 'locale_language' and 'locale_generate' are default.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: locale, tags: locale }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
