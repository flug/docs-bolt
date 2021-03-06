---
title: Upgrading from version 2.2 to 3.0
---
Upgrading a site from version 2.2 to 3.0
========================================

This page provides an indepth guide of how to move an existing 2.2.x site up to
the latest 3.0 release. Since this is a major release you cannot assume that
there will be no breaking changes and the complexity of the upgrade will vary a
lot depending on how much custom code you have in your current site.

You will definitely make the process smoother by taking the following precautions.

 1. Make sure you are on the latest stable release of the 2.2.x series
 2. Make sure that you do a full backup of the site database, uploaded files,
    config files and the extensions directory.
 3. If possible have your current install under git source control and test any
    changes on a new branch which can then easily be reverted.
 4. If you come across any undocumented issues, let us know by raising an issue
    on Github
 5. Check that the extensions you need have [versions available for Bolt 3.0][1]

There are basically two methods to update an existing installation. Pick the one that most closely resembles your current installation:

 - [Basic][basic]: This describes the process of setting up a fresh Bolt 3.0 install, and moving over all of your existing configuration, data, themes and uploaded media. Use it if you're using a common Bolt installation.
 - [Advanced][advanced]: This describes the process of converting an existing Bolt 2.2 install to Bolt 3.0. Use this method if you're running a non-default Bolt installation, like a customized Composer install.

We recommend the first option, because it allows you to get a fresh install up and running, without hassle or leaving behind too many old files.

[1]: http://extensions.bolt.cm/bolt3-ready
[basic]: moving-22-30-basic
[advanced]: moving-22-30-advanced
