.. Data Visualization documentation master file, created by
   sphinx-quickstart on Wed Aug 22 12:35:28 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Data Visualization!
==============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:


Welcome to Data Visualization. In this course you learn how to manipulate and visualize data to learn from it.
You learn from data when you are able to classify new instances or make predictions based on previous
experience. We'll be studying many example of data visualization and we'll look at getting data into the right format to
be analyzed.

An excellent textbook is "Data Visualisation: A Handbook for Data Driven Design" by Andy Kirk. The text
covers many of the principles and ideas necessary for good data analysis and visualization. This website
will outline some of his principles. More details can be found in his text.

Python Programming
---------------------

We'll start with some Python programming. Please take a look at these videos on Python programming. Watch them up through the video on reading XML files
in chapter 4. You can also consult the following websites for additional background on programming with
Python.

  * `Lectures on Python Programming <https://www.youtube.com/playlist?list=PL1DE477438120C9EF>`_
  * `Support Site for the Lectures on Python Programming <http://cs.luther.edu/~leekent/IntroToComputing>`_
  * `Additional Examples of Python Programming <http://cs.luther.edu/~leekent/CS2Plus>`_
  * `An online text on Python Programming <https://kentdlee.github.io/SCSI/build/html/index.html>`_
  * `You might also find this online text to be useful <http://interactivepython.org/runestone/static/thinkcspy/index.html>`_

If you want an additional textbook or textbooks on Python programming you can check out my two texts. The
first of these goes with the video lectures found above.

  * `Python Programming Fundamentals <https://www.amazon.com/Programming-Fundamentals-Undergraduate-Computer-Science/dp/1447166418>`_
  * `Data Structures and Algorithms with Python <https://www.amazon.com/Structures-Algorithms-Undergraduate-Computer-Science/dp/3319130714/ref=pd_sim_14_1?_encoding=UTF8&pd_rd_i=3319130714&pd_rd_r=43ee148a-aff3-11e8-ab28-01ad97aa66bb&pd_rd_w=gfZsy&pd_rd_wg=NhjP4&pf_rd_i=desktop-dp-sims&pf_rd_m=ATVPDKIKX0DER&pf_rd_p=18bb0b78-4200-49b9-ac91-f141d61a1780&pf_rd_r=6PP30YNX074T4S2FNGCP&pf_rd_s=desktop-dp-sims&pf_rd_t=40701&psc=1&refRID=6PP30YNX074T4S2FNGCP>`_

You want to get good at string manipulation, reading and writing XML files, and working with lists and dictionaries. Reading
JSON data, Beautiful Soup, and sending HTML requests with Python will be valuable skills to learn during
data collection. You need to also be good at reading and writing files.

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

Data Science starts with data. Good resources for data can be found at these sites.

* `http://bigdata-madesimple.com/70-amazing-and-free-data-sources-for-data-visualization/ <http://bigdata-madesimple.com/70-amazing-and-free-data-sources-for-data-visualization/>`_
* `http://kaggle.com <http://kaggle.com>`_
* `Google Dataset Search <http://toolbox.google.com/datasetsearch>`_

The Data Science Life Cycle
-------------------------------

Applying Data Science begins with a question. That is the most important part of data science, asking questions.
For many businesses the question probably revolves around revenue. Questions might be:

* Is there a more efficient way of doing this?
* What's the next big thing that we should be focusing on?
* Did we do a good job?
* How can we improve our product?
* How can we do it faster?

Questions like these are hard to answer and to answer them requires data to back up any claims that are
made. Asking a good question is difficult. Gathering the data to answer the question is at least ten
times harder. Most of the work in Data Science is in data acquisition.

`Microsoft has a good website detailing the lifecycle of a Data Science project <https://docs.microsoft.com/en-us/azure/machine-learning/team-data-science-process/lifecycle>`_. You should
take a look at this to understand the life cycle and in particular the data acquisition process described
on that page.

Visualization Workflow
------------------------

It is important to develop a visualization workflow. This workflow should be repeated (and improved on) with
each project. The process of developing a visualization is that of developing a compelling story/narrative
around the data. To be effective in generating this narrative, you need to observe the following.

  * Be pragmatic.
  * Reduce the randomness of your approach.
  * Protect experimentation.
  * Facilitate adaptability and iteration.
  * Develop a repeatable process.

To be successful using these principles, you need to take notes and use pen and paper to sketch out what
you intend to do. Note taking is important because creative thoughts come at odd times and need to be
written down to be available to you when you have time to build upon them. Manage your time and resources
well, but leave time for creative thinking. Sometimes pressures may cause you to develop some rules-of-thumb
for finding answers to some questions.

Be sure to communicate with your audience and stakeholders. Do your research. Pay attention to detail. Be
honest with yourself. And above all else, **learn**. We all need to work at **learning** as this
is a rapidly expanding field and you need to stay current.

So, here are some steps to take in developing this workflow.

#. Formulate a brief - According to Andy Kirk, a brief represents a set of expectations and captures all the relevant information about a task or project.
#. Start from curiosity. It might be your curiosity. It might be the curiosity of the stakeholder, your audience, or other potential intrigue of yet unidentified individuals.
#. Identify your audience. The idea of intrigue should be not only your intrigue. Your job is to create intrigue in your audience. This draws people in to the narrative and gives them a goal in understand your data visualization. Often presenting a question that is answered (at least in part) in the data can help create that intrigue.
#. Understand your contraints. Time constraints, tool constraints, All your constraints will factor into what you end up doing.
#. Understand how the work will be consumed. You especially want to know the frequency with which this visualization will need to be repeated. If it needs to be repeated frequently, the it should be as automated a process as possible. More attention to the process may be necessary if it will be frequently reproduced.

Data Acquisition
-----------------

Building a pipeline for data acquisition means writing code that can be used to acquire, munge, and
refresh the data as often as is necessary given the needs of the project. Automation of data acquisition
for a project is our goal. We want to write code to allow us to push a button to refresh large data
sets coming from multiple sources.

Munging data refers to writing a program (Python is an excellent choice for this) that massages the data
into a format that we can use in our data pipeline. The Pandas *Dataframe* has become very important
in managing data for a project. We'll first learn what a *Dataframe* is and how to build one.

The DataFrame
----------------

We start by learning to use notebooks and build dataframes in Pandas. `Take a look at this
example of creating a dataframe <notebooks/TheDataframe.ipynb>`_.

Munging Data with Python
---------------------------
Munging is sometimes called *Data Wrangling* or *Massaging the Data*. All terms mean the same thing. When we
get data from a source it is not always in the proper format for using all the tools that we want to use.

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

Data Acquisition
-------------------

We don't always get the data that we want in a file. Sometimes the data is available on the web and we need
to build our own data table. In that case we might use the `Python Requests Library <http://docs.python-requests.org/en/master/>`_.
This library is very
popular and is used widely for data acquisition.

The Requests library can be used for screen scraping. See this tutorial on `Screen Scraping with the
Requests Library <https://docs.python-guide.org/scenarios/scrape/>`_ for help on doing this. The other
common framework for screen scraping is called `BeautifulSoup <https://www.crummy.com/software/BeautifulSoup/bs4/doc/>`_.
You can `work through a tutorial on BeautifulSoup by clicking here <https://www.dataquest.io/blog/web-scraping-tutorial-python/>`_.


Another use of the Requests Library is for accessing API's on the web. An API is an Application
Programming Interface. A Web-based API is generally implemented as a RESTful API. RESTful interfaces
are servers on the internet that accept URL requests and respond with data in much the same way a web
server would respond to the request for an HTML page. However, the RESTful API service may respond with
a CSV or JSON file as its result.
`Read this tutorial <https://tutorialedge.net/python/python-http-requests-tutorial/>`_
to get started using the Requests Library to read data from a RESTful source.

You might need to see how to `access data via an xpath <notebooks/ParsingHTMLandusingXPath.ipynb>`_.

Building a Dataset with a Webcrawler
+++++++++++++++++++++++++++++++++++++++

`This tutorial takes you through an example of building a website with a Webcrawler application <https://towardsdatascience.com/data-analytics-with-python-by-web-scraping-illustration-with-cia-world-factbook-abbdaa687a84>`_. This can
work sometimes, but it depends on the website you are trying to access as some websites will not
want to provide information to a program. Programs written like this can *steal* another company's data
in seconds. So, it is often the case that webcrawler applications get flagged and webserver deny access
to them. The tutorial provide here is not subject to these problems.

Reading a JSON file to build a Dataframe
++++++++++++++++++++++++++++++++++++++++++

Reading JSON data is another skill you need as a data scientist. `This tutorial <https://www.dataquest.io/blog/python-json-tutorial/>`_ provides
a good introduction to reading JSON in your data acquisition program. You should take a look at this
notebook on how to install the ijson and possibly create your own environment in which to install
it.

Exercise 2
+++++++++++++

Pose a question. For instance, "Do increases in Avocado consumption predict increases in home sales?"
Write some screen scraper code, using the Requests Library and/or BeautifulSoup,
to gather information to help answer your question (not this avocado/home sales question, but your own question). Place the collected
data in a CSV file with proper headings. Describe the question, the collected data, and the program
used to collect the information.

Exercise 3
++++++++++++
Pose a question and query a RESTful API to gather information about the answer to that question. Use the
Requests Library to gather the information from the API and put it into a CSV file. In the Python program
write a comment at the top that indicates the question, the API being used, and the data that is being
collected to answer the posed question.

Exercise 4
++++++++++++

Pose a question that you need to gather a large dataset to either prove or disprove. Then go to the
web and find data that supports or disproves your hypothesis. You may use JSON data, XML data, a
webcrawler, or any means necessary to get acquire the data that you need.

Building a Website
------------------

Building a website like this one is actually very easy with the help of sphinx. To begin, you
open a terminal window and make a directory for yourself. Then you type *sphinx-quickstart* and
follow the prompts as shown here. You can take defaults for yourself for most prompts. The project
name should be your own project name and author is yourself of course.

.. code-block:: console

    Kent's Mac> mkdir MyWebSite
    Kent's Mac> cd MyWebSite
    Kent's Mac> sphinx-quickstart
    Welcome to the Sphinx 1.7.4 quickstart utility.

    Please enter values for the following settings (just press Enter to
    accept a default value, if one is given in brackets).

    Selected root path: .

    You have two options for placing the build directory for Sphinx output.
    Either, you use a directory "_build" within the root path, or you separate
    "source" and "build" directories within the root path.
    > Separate source and build directories (y/n) [n]:

    Inside the root directory, two more directories will be created; "_templates"
    for custom HTML templates and "_static" for custom stylesheets and other static
    files. You can enter another prefix (such as ".") to replace the underscore.
    > Name prefix for templates and static dir [_]:

    The project name will occur in several places in the built documentation.
    > Project name: My Website
    > Author name(s): Kent D. Lee
    > Project release []:

    If the documents are to be written in a language other than English,
    you can select a language here by its language code. Sphinx will then
    translate text that it generates into that language.

    For a list of supported codes, see
    http://sphinx-doc.org/config.html#confval-language.
    > Project language [en]:

    The file name suffix for source files. Commonly, this is either ".txt"
    or ".rst".  Only files with this suffix are considered documents.
    > Source file suffix [.rst]:

    One document is special in that it is considered the top node of the
    "contents tree", that is, it is the root of the hierarchical structure
    of the documents. Normally, this is "index", but if your "index"
    document is a custom template, you can also set this to another filename.
    > Name of your master document (without suffix) [index]:

    Sphinx can also add configuration for epub output:
    > Do you want to use the epub builder (y/n) [n]:
    Indicate which of the following Sphinx extensions should be enabled:
    > autodoc: automatically insert docstrings from modules (y/n) [n]:
    > doctest: automatically test code snippets in doctest blocks (y/n) [n]:
    > intersphinx: link between Sphinx documentation of different projects (y/n) [n]:
    > todo: write "todo" entries that can be shown or hidden on build (y/n) [n]:
    > coverage: checks for documentation coverage (y/n) [n]:
    > imgmath: include math, rendered as PNG or SVG images (y/n) [n]:
    > mathjax: include math, rendered in the browser by MathJax (y/n) [n]:
    > ifconfig: conditional inclusion of content based on config values (y/n) [n]:
    > viewcode: include links to the source code of documented Python objects (y/n) [n]:
    > githubpages: create .nojekyll file to publish the document on GitHub pages (y/n) [n]:

    A Makefile and a Windows command file can be generated for you so that you
    only have to run e.g. `make html' instead of invoking sphinx-build
    directly.
    > Create Makefile? (y/n) [y]:
    > Create Windows command file? (y/n) [y]:

    Creating file ./conf.py.
    Creating file ./index.rst.
    Creating file ./Makefile.
    Creating file ./make.bat.

    Finished: An initial directory structure has been created.

    You should now populate your master file ./index.rst and create other documentation
    source files. Use the Makefile to build the docs, like so:
       make builder
    where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

    Kent's Mac>

You edit text according to the sphinx markdown language. Sphinx markdown is well-documented on the web.
You can see examples of how sphinx pages are written if you go to `https://github.com/kentdlee/SCSI <https://github.com/kentdlee/SCSI>`_.
This repository has a *build* and a *source* directory. The *source* directory contains the source file *index.rst*
which is where the content is located. The *build* directory contains a subdirectory called *html* which
can be copied to a webserver. The *html* directory would be renamed whatever you would want your site called.
For instance, if you wanted to call it *MyWebSite* then you would copy the html directory into your *public_html*
on your webserver and rename the html to *MyWebSite*.

Hosting on Github.com
++++++++++++++++++++++++

You can also host the website on Github.com. To do this, you'll want to create an SSH key for transferring
files to and from Github.com. On a Mac you can `follow this guide to generate an SSH key <https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/>`_.
This guide shows you how to create the key and then copy the public
key to another computer. For Github.com you go to your account *Settings* (top right corner of Github.com page after
you sign in). Then click on *SSH and GPG keys*. Click the *New SSH key* button
and paste your public key into that directory.

On a Windows machine, you need to `install git bash from here <https://git-scm.com/downloads>`_. Then
you can `follow the directions here <https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows>`_
to generate a key and add it to your Github.com account (see the link at the end of the page).

After setting up a key on Github.com you can create a repository to hold your website. Create a normal
repository, but in the settings for the repository change the section *GitHub Pages* to say that the source
is on the master branch. Have the repository create a README.md file.

Then add anyone who will be collaborating with your by clicking on *Settings* for your repository on GitHub.com and add
the collaborator(s). Make sure you give them editing capability.

Now, both collaborators can do the following. Go to a folder where you want to hold the website. You can open a terminal
window (or gitbash terminal in Windows) and change to that directory/folder. Then execute the following where *username*
is your username and *MyWebSite* is the name of your repository.

.. code-block:: console

      Kent's Mac> git clone git@github.com:username/MyWebSite.git
      Kent's Mac>

Then move all files from your website (if you previously created the files) into this new directory/folder. You can use this command
to do that on a Mac or in gitbash on a PC.

.. code-block:: console

    Kent's Mac> cd MyWebSite
    Kent's Mac> mv path/to/olddir/* .

This will move all files to your new *MyWebSite* folder.
In the *MyWebSite* directory you will need to create two additional files. You can create them by doing these commands.

.. code-block:: console

    Kent's Mac> cd MyWebSite
    Kent's Mac> echo "<meta http-equiv=\"refresh\" content=\"0; url=build/html/index.html\" />" > index.html
    Kent's Mac> touch .nojekyll


The index.html file contains the redirect to your build/html/index.html directory. If you have *_build* instead of *build* for
your sphinx build directory, then change the name above. This redirect means that when
someone loads this web page in the home directory of the project, it will redirect to the github.com
webpage address for this page (i.e. in the build directory).

There must be a file in the home directory of the website called .nojekyll. This tells GitHub.com not
to process this webpage with jekyll which is another markdown formatter. The *touch* command above created
that file.

Finally, you can add the following lines into your Makefile. This will allow you to type *Make release* to
send it to GitHub.com and the world. You can open the website after a few minutes (it takes a few minutes to update on
the web). Your repository settings tell you the URL of the GitHub page to open.

.. code-block:: console

    release: html
            git add .
            git commit -m "latest changes"
            git push -u origin master

On a windows machine you can create a batch file with the last three lines of the file given above to execute in your gitbash
shell. You can call this batch file *release.bat*. Then to run it you type *release* to release it to the world.


Common Graph Types
---------------------

Here are some guides to building various graphs.

Stacked Area Plots
++++++++++++++++++++++++++++++

`In this notebook <notebooks/Introduction\ to\ Plotting\ Exercise.ipynb>`_ I work with the `movie database <_static/movies.csv>`_ to build a stacked area plot and a few other example graphs. Perhaps one of the most important parts of this notebook is in creating a pivot_table which takes columns from a DataFrame and builds a new DataFrame from it where the values in a column become columns in a new DataFrame.

Box and Whisker Plots
+++++++++++++++++++++++

`In this notebook <notebooks/Shared\ Bike\ Service\ Data.ipynb>`_ you learn about Box and Whisker Plots and how they can be used to examine the same of data in a column.

Bubble Plots
+++++++++++++

`Here we create a Bubble Plot <notebooks/Shared%20Bike%20Service%20Data.ipynb#Bubble-Plot>`_ which can help to visualize
three-dimensional data.

Violin Plots
++++++++++++

`A Violin Plot is like a box and whisker plot but shows the distribution of data within the range of possible values <notebooks/Shared%20Bike%20Service%20Data.ipynb#Violin-Plot>`_.
For this kind of plot we use the Seaborn library since it contains a nice violin plotting function.

Heatmap Plots
++++++++++++++

`A Heatmap is a way to plot 3 dimensional data where the two axis dimensions are categorical <notebooks/Shared%20Bike%20Service%20Data.ipynb#Heat-Map>`_.
This kind of plot also uses the Seaborn library for its heat map plotting function.

Network Graph
++++++++++++++

Sometimes called a node-link graph, this kind of plot shows connections between categorical information. For instance in `this
notebook the connections between technogies are plotted <notebooks/Stackoverflow%20Technology%20Connections.ipynb>`_.

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
