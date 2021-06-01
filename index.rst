jupyter.cs for teachers
=======================

https://jupyter.cs.aalto.fi is a service for

* light computation
* with Jupyter notebooks running on a Linux system
* which provides some nice features for assignments
* but is **not** a "learning management system"
* built of **standard** open-source components.

Components
----------



What is Jupyter?
~~~~~~~~~~~~~~~~

* A system for interactive computing: "notebooks"

  * Text, code, outputs all together

  * ``echo "command" | python | web-browser``

* Low barrier to programming, great for courses

* Great for experimenting, not great for production work.

* Not just Python


.. note::

   This talk assumes you know Jupyter, I am not going into the details
   of it here.



What is JupyterHub?
~~~~~~~~~~~~~~~~~~~

* A multi-user Jupyter resource manager
* Allocates resources and starts regular Jupyter - nothing fancy!



JupyterHub is not:

- User accounts (depends on configuration)
- Data storage (depends on environment it starts)
- Compute power (depends on environment it starts)
- Programming language (see `Jupyter kernels <https://github.com/jupyter/jupyter/wiki/Jupyter-kernels>`__)



Aalto integration
~~~~~~~~~~~~~~~~~

jupyter.cs connects to Aalto services:

- Users: Aalto accounts (same as Aalto shell servers)
- Data storage: Network drive

  - Also mounted on shell servers
  - Also mountable on your own laptop: smb://jhnas.org.aalto.fi

- Compute: CS kubernetes cluster
- Programming language: conda environments in Docker images

**jupyter.cs is not dedicated for courses and nothing else.  This is
the advantage *and* disadvantage.**



What is nbgrader?
~~~~~~~~~~~~~~~~~
"notebook grader" is a system for

- Creating assignments in notebooks
- (Distributing them to students and getting them back)
- Autograding
- Manual grading
- **Not** a learning management system

  - More like a bunch of scripts for managing the **standard format**
    notebook files.

It is **not** a fancy tool, and the simplicity is the value.


Nbgrader demo
~~~~~~~~~~~~~

* Create a notebook
* Add basic function
* Add test of function
* Add ``### {BEGIN,END} SOLUTION``
* Add ``### {BEGIN,END} HIDDEN TESTS``
* Release / fetch / solve / validate / submit / collect
* Grading: auto and manual
* Getting grades out



How can jupyter.cs be used in your teaching?
--------------------------------------------

There are three different levels:

* **Computing environment only**, no nbgrader
* Computing environment, **nbgrader just to distribute files**
* Computing environment + **nbgrader grading**


Computing environment only
~~~~~~~~~~~~~~~~~~~~~~~~~~

Students are given jupyter.cs as an option to do their work/projects,
but it's not the only option.

Solves problems:

* Difficult to install software, you need a way that works for everyone
* People need a Linux environment
* You have big data, don't want everyone to have to make a copy



nbgrader for file distribution
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You use nbgrader to release assignments (but can release them other
ways, too), students do their work and submit assignments however they
normally would.

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
* If you use nbgrader, prepare to put in some time to it.


Encourage the department to support it
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* The Aplus system gets many resources.  jupyter.cs gets almost none.
* Plenty of this is my (rkdarst's) fault for not reaching out to
  teachers enough
* Minimum: a summer worker to deal with some of the more annoying but
  easy-to-fix UI issues
* GPUs: big question mark, not cost-effective to deploy.



Other options
~~~~~~~~~~~~~

* Aalto ITS / Learning services is making a JupyterHub

  * Do they know of nbgrader?  Do they have good data services?
  * Jupyter is easy, good computational environment is harder.

* Integrate with Aplus for autograding

  * They are so different I really don't know how this would work.
  * Unrelated to many of the UI issues

* CSC options

  * In past has seemed more like a standalone computing environment.



Are these things valuable to you?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Network drive for data storage, available on your own computers
* Persistent user data (not deleted per-course)
* Persistent course data
* Ability to use outside of courses

If these are not valuable, there is little need for jupyter.cs.


(advertisement: Do your students like basic non-scientific computing
skills?  The Science-IT project https://handsonscicomp.readthedocs.io/
is an online course which may be useful!)



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
