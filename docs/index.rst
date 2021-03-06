apex_stats's documentation!
======================================
| Y a y

-----------------------

Contents
==================

* Usage_

* FAQ_

* License_

-----------------------

.. _Usage:


**Usage**
==========
| Usage for the library apex_stats

| Before using this library make sure you don't import the whole library, rather the part you need. E.g. let's say I need full user info, therefore I do this:

.. code-block:: python
   :linenos:

    from apex_stats import User
    user = User("api-key", "username")
    ....

**Stats("tracker.gg-api-key")**
===============================

|  Gets specific information about a user(W.I.P. at the moment as I will add more functions at a later stage)

| For the sake of the docs we will assign a variable to the initiation of the class like so:

.. code-block:: python
    :linenos:

    apexInstance = apex.Stats("your-tracker.gg-api-key")

  
recentlyPlayed(username/id, userplatform)
#########################################

| Returns 5 of your recently played legends as a list.

| **username/id** - the desired username to get data from.

| **userplatform** -  default=origin, choose from 'origin', 'xbl', 'psn'.

.. code-block:: python
   :linenos:


    apexStats = apexInstance.recentlyPlayed("testuser")

    print(apexStats)

    >>> ['your', 'last', 'played', 'characters']


matchHistory(username/id, gamecount, userplatfom)
#####################################################

| Returns data from x number of games.

| **username/id** - the desired username to get data from.

| **userplatform** -  default=origin, choose from 'origin', 'xbl', 'psn'.

| **gamecount** - number of games you want data from (counted from your last game)

.. code-block:: python
   :linenos:

    apexHistory = apexInstance.matchHistory("testuser", 2)

    print(apexStats)

    >>> [{game1:legend, game1:kills, game1:duration},
    {game2:legend, game2:kills, game2:duration}]

-----------------------

**User("tracker.gg-api-key", "username-to-look-up", "platform(optional)"**
==========================================================================
| Dumps jsons with lots of information about given user.

| **username-to-look-up** - the desired username to get data from.

| **platform** -  default=origin, choose from 'origin', 'xbl', 'psn'.

| For the sake of the example, let's assign a variable:

.. code-block:: python
    :linenos:
    apexInstance = apex.User("tracker.gg-api-key","testuser")


games
#####################################################

| Returns around 3 of given user's matches

.. code-block:: python
    :linenos:

    apexStats = apexInstance.games

    print(apexStats)

    >>> {"info about":"matches"}


stats
#####################################################

| Returns user information like rank, kills, damage, etc

.. code-block:: python
    :linenos:

    apexStats = apexInstance.stats

    print(apexStats)

    >>> {"info about":"user", "rank":"gold"}

-----------------------

.. _FAQ:

**FAQ**
========

Who is behind this
##################

| I am a high school student starting out in coding. This is a fun little project I thought of while making a discord_ bot to practice.

.. _discord: https://github.com/refresher/nansense13/tree/master/discord

Why did you make docs AND a package when this is useless
########################################################

| Because **practice**. I need a **lot** of practice.

This page is useless
####################

I know. Go back_?

.. _back: https://google.com


.. _License:

License
=======

MIT License

Copyright (c) 2020 Yamozha

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
    