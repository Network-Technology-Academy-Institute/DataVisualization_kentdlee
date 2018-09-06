.. Data Visualization documentation master file, created by
   sphinx-quickstart on Wed Aug 22 12:35:28 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Data Visualization!
==============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   notebooks/TheDataframe.ipynb

Welcome to Data Visualization. In this course you learn how to manipulate and visualize data to learn from it.
You learn from data when you are able to classify new instances or make predictions based on previous
experience. We'll be studying many example of data visualization and we'll look at getting data into the right format to
be analyzed. We'll start with some Python programming.

Python Programming
---------------------

Please take a look at these videos on Python programming. Watch them up through the video on reading XML files
in chapter 4. You can also consult the following websites for additional background on programming with
Python.

  * `Lectures on Python Programming <https://www.youtube.com/playlist?list=PL1DE477438120C9EF>`_
  * `Support Site for the Lectures on Python Programming <http://cs.luther.edu/~leekent/IntroToComputing>`_
  * `Additional Examples of Python Programming <http://cs.luther.edu/~leekent/CS2Plus>`_
  * `An online text on Python Programming <https://kentdlee.github.io/SCSI/build/html/index.html>`_
  * `You might also find this online text to be useful <http://interactivepython.org/runestone/static/thinkcspy/index.html>`_

If you want an additional textbook or textbooks on Python programming you can checkout my two texts. The
first of these goes with the video lectures found above.

  * `Python Programming Fundamentals <https://www.amazon.com/Programming-Fundamentals-Undergraduate-Computer-Science/dp/1447166418>`_
  * `Data Structures and Algorithms with Python <https://www.amazon.com/Structures-Algorithms-Undergraduate-Computer-Science/dp/3319130714/ref=pd_sim_14_1?_encoding=UTF8&pd_rd_i=3319130714&pd_rd_r=43ee148a-aff3-11e8-ab28-01ad97aa66bb&pd_rd_w=gfZsy&pd_rd_wg=NhjP4&pf_rd_i=desktop-dp-sims&pf_rd_m=ATVPDKIKX0DER&pf_rd_p=18bb0b78-4200-49b9-ac91-f141d61a1780&pf_rd_r=6PP30YNX074T4S2FNGCP&pf_rd_s=desktop-dp-sims&pf_rd_t=40701&psc=1&refRID=6PP30YNX074T4S2FNGCP>`_

You want to get good at string manipulation, reading and writing XML files, and working with lists and dictionaries.
You need to also be good at reading and writing files.

Computer Architecture and Performance
-----------------------------------------

There are a few things you need to learn about computer architecture given that we will often be
dealing with large amounts of data. When we are ready to work with a large amount of data we need to be
cognizant of a few things about computers. CPUs are fastest. Memory is slower then a CPU but faster than a
disk drive. Disk drives and accessing data over the internet are much slower than memory as depicted here.

.. figure:: https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter1/1_4_StorageDeviceHierarchy.jpg

Caching can make some programs appear to run faster. A cache is a smaller (i.e. faster, more expensive)
memory that can be used to hold data that the computer thinks has a reasonable chance of being used soon.

.. figure:: https://qph.fs.quoracdn.net/main-qimg-64d592b11dc2b5c990fc6e10e9396b93.webp

Here are some sources of information about Computer Architecture and how it affects the performance of
dealing with big data.

  * `Dealing with Big Data and Databases <https://queue.acm.org/detail.cfm?id=1563874>`_ this text is an
    excellent description of some of the challenges of working with big data, especially when it resides
    in a database.

  * `Moore's Law <https://en.wikipedia.org/wiki/Moore%27s_law>`_ deals with the doubling of memory capacity
    as the number of transistors doubles around every two years. This means that we can expect to see
    continued growth in the size of data that can be stored on hard drives and in the memory of a computer.

  * While SSD's are fast, DRAM (the memory of a computer) is typically about 5-10 times faster. An SSD
    might read data at 100-150 MB/second or faster. A 500GB Samsung SSD has a sequential read speed of
    550 MB/second. This is much slower than DRAM which can be read at somewhere around 1927 MB/second
    and if the data is cached, then data could be read as fast as 3748 MB/second. `See this site for a
    discussion of this <https://superuser.com/questions/1173675/how-much-faster-is-memory-ram-compared-to-ssd-for-random-access/1173713>`_.

There are a few other factors in how our programs will run when dealing with big data. One factor is called
*Computational Complexity* and it is the study of how efficiently our programs are written. Nothing, not
even the fastest CPU, can overcome a poorly written program. We must write our programs efficiently and in
terms of computational complexity that means to be aware of any loops you write in a program.

We must also be concerned about issues like how many times you access a file on disk, how
much of the main memory (RAM or DRAM) you are using in your program, and how often you move data back and
forth from the disk into memory. Sometimes you may not even be aware that you are moving data from DRAM
to disk because of something called virtual memory that uses the disk to hold the contents of DRAM when
you don't have enough DRAM to contain all the data in your program at one time.

Another big issue that affects the performance of our programs is what language the program is implemented
with. We will write Python code, but whenever possible we should rely on library code to do something for
us rather than writing Python code to do it ourselves. Libraries are often implemented in C and run much
faster than Python code.

All of these considerations factor into the performance of our programs. And often times it is a job
that is best left to experts in the field, but sometimes writing our own code is unavoidable. Much of
the recent work in Data Science has been toward optimizing algorithms that deal with large amounts of
data to get the absolute best performance possible.

The Moral of the Story
++++++++++++++++++++++++

Whenever possible, we are going to want to rely on a library or module to do a computation for us. As a
last resort we should rely on writing significant Python code ourselves. Modules that we use are
sometimes written in C, not Python. In addition, modules have often been optimized to work with disk
and memory by caching information and/or reading from disk only when absolutely necessary. And, modules
will often be written to read from disk only once rather than read data inefficiently.

Thankfully, there are many modules
that have now been written to be as efficient as possible when dealing with large amounts of data. We
will be learning about several of these modules or libraries this semester.

Data Science
---------------

What is Data Science?

.. figure:: https://cdn-images-1.medium.com/max/1000/1*mgXvzNcwfpnBawI6XTkVRg.png

Data Science starts with data. A good resource of data can be found at these two sites.

* `http://bigdata-madesimple.com/70-amazing-and-free-data-sources-for-data-visualization/ <http://bigdata-madesimple.com/70-amazing-and-free-data-sources-for-data-visualization/>`_
* `http://kaggle.com <http://kaggle.com>`_

Munging Data with Python
--------------------------

Consider the Avocado data set which can be found on Kaggle here.

`https://www.kaggle.com/neuromusic/avocado-prices#avocado.csv <https://www.kaggle.com/neuromusic/avocado-prices#avocado.csv>`_

You can download this data set from here.

`http://cs.luther.edu/~leekent/avocado.csv <http://cs.luther.edu/~leekent/avocado.csv>`_

This is a CSV (Comma Separated Values) file. It can be read by a Python program like the one below. The
file and the program need to be saved in the same folder or directory to run this program.

Note the use of the *split* method below with a comma as the separator.

.. code-block:: python

    def main():
        file = open("avocado.csv")
        for line in file:
            x = line.strip()
            lst = x.split(",")
            print(lst)


    if __name__ == "__main__":
        main()


The file can also be read from the internet directly if you know the URL. The urllib.request module
is a Python3 module that allows you to open a file on the web. When the file is downloaded it is
in unicode format. So, *decode* must be called on anything that is read in this format.

Take a look at the code below. It contains some extra code for taking apart the fields in a CSV file
and then putting them back together. In between taking the CSV records apart and putting them back
together you can do any processing that you might need to do to get your data ready for some further
analysis.

.. code-block:: python

    import urllib.request

    def main():
        file = urllib.request.urlopen("http://cs.luther.edu/~leekent/avocado.csv")
        for line in file:
            x = line.strip()
            lst = x.decode('utf-8').split(",")
            # Fix anything that needs fixing in the data.
            # Your code goes here for fixing/gathering data.
            # Then you start rebuilding the string to recreate the fixed up file.
            lst = [x+"," for x in lst]
            # Write a new file? Print will work if you redirect output.
            # The [:-1] on the resulting string removes the last comma.
            print("".join(lst)[:-1])


    if __name__ == "__main__":
        main()


The DataFrame
-----------------
We start by learning to use notebooks and build dataframes in Pandas. `Take a look at this
example of creating a dataframe <notebooks/TheDataframe.ipynb>`_.


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
