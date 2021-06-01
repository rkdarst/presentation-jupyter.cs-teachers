jupyter.cs for teachers
=======================

Components
----------



What is Jupyter?
~~~~~~~~~~~~~~~~



What is JupyterHub?
~~~~~~~~~~~~~~~~~~~



What is JupyterHub not?
~~~~~~~~~~~~~~~~~~~~~~~
- User accounts
- Data storage
- Compute power
- Programming language



Aalto integration
----------------
- users: Aalto accounts (same as Aalto shell servers)
- Data storage: Network drive

  - Also mounted on shell servers
  - Also mountable on your own laptop: smb://jhnas.org.aalto.fi

- Compute: CS kubernetes cluster
- Programming language: conda environments in Docker images



What is nbgrader?
~~~~~~~~~~~~~~~~~
System for

- Creating assignments in notebooks
- (Distributing them to students and getting them back)
- Autograding
- Manual grading


Nbgrader demo
~~~~~~~~~~~~~


How can it be used in your teaching?
------------------------------------

There are three different levels:

* **Computing environment only**, no nbgrader
* Computing environment, **nbgrader just to distribute files**
* Computing environment + **nbgrader grading**


Computing environment only
~~~~~~~~~~~~~~~~~~~~~~~~~~
Solves problems:

* Difficult to install software, you need a way that works for everyone
* People need a Linux environment for scripting
* You have big data, don't want everyone to have to make a copy

nbgrader for file distribution
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Solves problems:

* Computing environment from above
* Easily distributes files in a way they can be directly run

nbgrader + autograding
~~~~~~~~~~~~~~~~~~~~~~

Solves problems:

* Complete course

Complexities:

* You have to design your assignments like they will be unit tested
* nbgrader quirks



Future
------

If you want to use it
~~~~~~~~~~~~~~~~~~~~~

* Read the instructor's guide:
  https://scicomp.aalto.fi/aalto/jupyterhub-instructors/
* Contact guru@cs.aalto.fi for help
* In practice, it is Richard almost alone supporting this these days.


Encourage the department to support it
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* The Aplus system gets many resources.  jupyter.cs gets almost none.

*

Are these things valuable to you?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Network drive for data storage, available other ways
* Persistent user data (not deleted per-course)
* Ability to use outside of courses



..
  .. toctree::
     :maxdepth: 2
     :caption: Contents:



..
   Indices and tables
   ==================

   * :ref:`genindex`
   * :ref:`modindex`
   * :ref:`search`
