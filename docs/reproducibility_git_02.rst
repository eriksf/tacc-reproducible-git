
The Basics of Git
-----------------

Version control systems start with a base version of the document and
then record changes you make each step of the way. You can
think of it as a recording of your progress: you can rewind to start at the base
document and play back each change you made, eventually arriving at your
more recent version.


.. image:: ./images/play-changes.svg
   :target: ./images/play-changes.svg
   :alt: Changes Are Saved Sequentially


Once you think of changes as separate from the document itself, you
can then think about "playing back" different sets of changes on the base document, ultimately
resulting in different versions of that document. For example, two users can make independent
sets of changes on the same document.


.. image:: ./images/versions.svg
   :target: ./images/versions.svg
   :alt: Different Versions Can be Saved


Unless there are conflicts, you can even incorporate two sets of changes into the same base document.


.. image:: ./images/merge.svg
   :target: ./images/merge.svg
   :alt: Multiple Versions Can be Merged


A version control system is a tool that keeps track of these changes for us,
effectively creating different versions of our files. It allows us to
decide which changes will be made to the next version (each record of these changes is called a
"commit", and keeps useful metadata about them. The
complete history of commits for a particular project and their metadata make up
a "repository". Repositories can be kept in sync
across different computers, facilitating collaboration among different people.

Setting up Git
^^^^^^^^^^^^^^

Use your local machine (or log on to one of the TACC systems, i.e. Frontera), and check which version of Git is in your ``PATH``.

.. note::
   Below, replace ``username`` with your TACC username.

.. code-block:: console

   $ ssh <username>@frontera.tacc.utexas.edu   # use your account
   (enter password)
   (enter token)

   $ which git
   /opt/apps/git/2.24.1/bin/git
   $ git --version
   git version 2.24.1

When we use Git on a new computer for the first time,
we need to configure a few things. Below are a few examples
of configurations we will set as we get started with Git:


* our name and email address,
* and that we want to use these settings globally (i.e. for every project).

On a command line, Git commands are written as ``git verb``\ ,
where ``verb`` is what we actually want to do. So here is how
we set up our environment on Frontera:

.. code-block:: console

   $ git config --global user.name "Erik Ferlanti"
   $ git config --global user.email "eferlanti@tacc.utexas.edu"

Please use your own name and email address. This user name and email will be associated with your subsequent Git activity,
which means that any changes pushed to
`GitHub <https://github.com/>`_\ ,
`BitBucket <https://bitbucket.org/>`_\ ,
`GitLab <https://gitlab.com/>`_ or
another Git host server
in the future will include this information.

.. tip::

   A key benefit of Git is that it is platform agnostic. You can use it equally to interact with the same files from your laptop, from a lab computer, or from a cluster. If needed, instructions to install Git locally can be found `here <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>`_.
