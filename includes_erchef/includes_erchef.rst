.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Starting with the release of |chef 11|, the front-end for the |chef server| is written using `Erlang <http://www.erlang.org/>`_, which is a programming language that `first appeared in 1986 <http://en.wikipedia.org/wiki/Erlang_%28programming_language%29>`_, was open sourced in 1998, and is excellent with critical enterprise concerns like concurrency, fault-tolerance, and distributed environments. This allows the new |chef server| to scale to the size of any enterprise.

This version of |chef| is often referred to as |erchef|. |erchef| is a complete rewrite of the core API for the |chef server|, which allows it to be faster and more scalable than previous versions. The API itself is still compatible with the original |ruby|-based |chef server|, which means that cookbooks and recipes that were authored for the |ruby|-based |chef server| will continue to work on the |erlang|-based |chef server|. The |chef client| is still written in |ruby|.

.. note:: Even though |chef 11| is authored in |erlang|, writing code in |erlang| is NOT a requirement for using |chef 11|.
