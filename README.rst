####################
IS 210 Assignment 06
####################
************
Warmup Tasks
************

:College: CUNY School of Professional Studies
:Course-Name: Software Application Programming I
:Course-Code: IS 210

Overview
========

Combined with Python's data structures, Python's library of looping techniques
allow for the efficient processing of massive amounts of data.

Instructions
============


.. important::

    In these exercises, you may, on occasion, come across a task that requres
    you to research or use a function or method not directly covered by the
    course text. Since Python is such a large language it would be impossible
    for the author to have included descriptions of each and every available
    function which would largely duplicate the offical Python documentation.

    A *vital* skill to successful programming is being comfortable searching
    for and using official language documentation sources like the
    `Python String Documentation`_ page. Throughout our coursework we will be
    practicing both the use of the language in practice and the search skills
    necessary to become functional programmers.

Warmup Tasks
============

Task 01
-------

In this task, we're going to build a Fibonacci sequence generator function with
our ``while`` loop.

Specifications
^^^^^^^^^^^^^^

1.  Begin by considering the following statement:

    .. code:: python

        lastnum, curnum = curnum, lastnum + curnum

    This is a Python trait known as *multiple assignment* and is part of the
    magic of tuple unpacking since the right side of the assignment operator is
    a tuple (without its parentheses). This is is a key feature of our
    particular implementation since the following is **not** equivalent:

    .. code:: python

        lastnum = curnum
        curnum = lastnum + curnum

    Note how, on the first line, the value of ``lastnum`` is changed so that
    its value is no longer valid for the ``curnum`` assignment.

    The benefit of multliple assignment in our scenario is that both
    variables may be assigned simultaneously, **before** their values change.

    Looped, this is the heart of the fibonacci sequence better illustrated at:

    https://docs.python.org/3/tutorial/introduction.html#first-steps-towards-programming

    We'll be performing a similar loop but doing so in a more programmatic
    manner.

2.  Open a new Jupyter notebook

3.  Create a new function named ``fibonacci()`` that takes one required
    parameter:

    1.  ``maxint``, an integer that will serve as the upper bound of the loop

4.  Following the example on the Python tutorial:

    https://docs.python.org/3/tutorial/introduction.html#first-steps-towards-programming

    Our implementation will have a few changes:

    1.  While you will use a ``while`` loop to make a Fibonacci sequence, the
        upper bound of the sequence will be your ``maxint`` parameter.

    2.  Store the results into a list and append each new generated number

5.  Return the newly generated sequence as a list.

.. note::

    In our example we are choosing to include the initial ``0`` value.

Expected Output
^^^^^^^^

.. code:: pycon

    >>> fibonacci(10)
    [0, 1, 1, 2, 3, 5, 8]

Task 02
-------

In this task, you'll be asked to create a simple for-loop to loop over a simple
data construct, in this case, to provide the maximum, minimum, and average
length of words in a speech performing a lexicographical analysis not unlike
what's used to measure reading level.

Specifications
^^^^^^^^^^^^^^

1.  Keep working on the same notebook

2.  Create a function named ``lexicographics()`` that takes one parameter:

    1.  ``to_analyze``, a **required** string

3.  Using a single ``for`` loop, calculate the following for your text:

    #.  The maximum number of words **per line** in ``to_analyze`` (eg, the
        length of the longest line in ``to_analyze``)

    #.  The minimum number of words **per line** in ``to_analyze`` (eg, the
        length of the shortest line in ``to_analyze``)

    #.  The average number of words **per line** in ``to_analyze``, stored
        as a decimal.

4.  Return these values as a tuple, in the order in which they are defined
    above.

.. hint::

    As with other for-loop endeavors, you'll need to set up some variables
    outside of your loop to catch your data as you process it.

.. hint::

    You'll have to ``split()`` the string twice to accomplish this task. First
    split it on just the newline (``\n``) to produce an iterable list of
    lines. As you iterate each line, you can then use ``split()`` again
    without any parameters to count the number of words.

.. tip::

    There are at least two good ways to solve this problem each with their
    own benefits. One way uses the ``max()``, ``min()`` and ``sum()`` functions
    to operate on a list, and the other involves using ``if`` to set-up running
    totals. Either are acceptable routes.

Expected Output
^^^^^^^^

.. code:: pycon

    >>> lexicographics('''Don't stop believing,
    Hold on to that feeling.''')
    (5, 3, Decimal(4.0))

Submission
==========

Code should be submitted via Blackboard as a python notebook.   

.. _GitHub: https://github.com/
.. _Python String Documentation: https://docs.python.org/2/library/stdtypes.html
