project description
-------------------------------

this project will ultimately run in a docker swarm. It consists of:
- an engine that computes the game of life for a grid & a pattern
- a server that presents the results (eventually for a bunch of engines running in parallele)
- eventually hosted on aws/linode or somthing similar

architecture
-----------------------

MVP
^^^^^^^^^^


server
~~~~~~~~~~~~~~~

* a simple flask server
* initially at least just a single page:
    * displays the engines that are running (metadata etc.)

docker-swarm
~~~~~~~~~~~~~~~~~~

* starts up the server & the engine with a manager
* ensures they talk

engine
~~~~~~~~~~~~

* initially just the implementation of the game of life from `geeks for geeks <https://www.geeksforgeeks.org/conways-game-life-python-implementation/>`_


Potential additions
^^^^^^^^^^^^^^^^^^^^^^^

server
~~~~~~~~~~~~~~~

* dispaly more stuff:
    * images/graphs/maps of the results, main stable patterns, etc.
    * add the ability to control the num of running engines with some panel

docker-swarm
~~~~~~~~~~~~~~~~~~

* actually control the replication dynamically

engine
~~~~~~~~~~~~
* compute results 