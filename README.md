Python and R resources for beginners...
=======================================

...with special regards to science and data analysis applications, visualization and graphics
---------------------------------------------------------------------------------------------

This collection has been started by
[Dávid Fazekas](mailto:fazekasda@gmail.com) and continued by
[Dénes Türei](mailto:turei.denes@gmail.com).
Submissions are welcome.

-   [Python and R resources for
    beginners...](#python-and-r-resources-for-beginners...)
    -   [Setting up a Python
        environment](#setting-up-a-python-environment)
    -   [Where to start?](#where-to-start)
    -   [Non Python specific but important
        resources](#non-python-specific-but-important-resources)
    -   [Interactive Python learning
        platforms](#interactive-python-learning-platforms)
    -   [Programming exercises](#programming-exercises)
    -   [Python tutorials](#python-tutorials)
    -   [Python resources](#python-resources)
    -   [Online Courses](#online-courses)
    -   [Python environments](#python-environments)
    -   [Python modules for data analysis](#python-modules-for-data-analysis)
    -   [Python visualization and
        plotting](#python-visualization-and-plotting)
    -   [Graphs (networks)](#graphs-networks)
    -   [Alternative network visuzalizations](#alternative-network-visualizations)
    -   [Visualization in general](#visualization-in-general)
    -   [Other tools for graphics and typography: post processing
        figures, designing slides, posters and figures, typesetting
        reports, papers, theses and
        books](#other-tools-for-graphics-and-typography-post-processing-figures-designing-slides-posters-and-figures-typesetting-reports-papers-theses-and-books)
    -   [R blogs and tutorials](#r-blogs-and-tutorials)
    -   [Statistics](#statistics)
    -   [IDEs (integrated development
        environments)](#ides-integrated-development-environments)
        -   [Python IDEs](#python-ides)
        -   [R IDEs](#r-ides)
    -   [Image processing](#image-processing)
    -   [Chemistry](#chemistry)
    -   [Books](#books)
        -   [Python beginner and intermediate books](#python-beginner-and-intermediate-books)
        -   [Advanced Python](#advanced-python)
        -   [R books](#r-books)
    -   [Lectures](#lectures)
    -   [Podcasts](#podcasts)
    -   [Miscellanous](#miscellanous)
    -   [Regular expression resources](#regular-expression-resources)
    -   [awk, sed, grep](#awk-sed-grep)

# Python and R resources for beginners...

## ...with special regards to science and data analysis applications, visualization and graphics

Here you find a list of useful resources for learning Python or R, as
well as a virtual environment where many tools are readily available for
you. You will find this collection helpful either if you are a scientist
and you just realized that you need computational tools for processing
your data, or you already have done it for a while but looking for new
tools and alternatives, or you just would like to start learning Python
or R for any other purpose.

## Setting up a Python environment

This repo contains a virtual environment created by David Fazekas and set up
for easy installation. It is unmaintained for a couple of years already, I can
not guarantee it works. The idea of this virtual environment is that you can
start using Python without learning how to install Python and modules, which
is not always straightforward and might even require some system
administration knowledge. Of course later you can learn these, but the virtual
environment provides a little help for a quick start. To install this
environment to your own computer follow
[the description](https://github.com/deeenes/bioinfo-tools/tree/master/JupyterEnv).

Alternatively you can install Python and modules the traditional way.
See below.

### General points

-   Python has two major versions available: Python 2 and 3. These are
    incompatible, although it is possible to write code which runs both in
    2 and 3. If you have both of them installed they will reside in their
    own directories and you install modules for them independently.
    It is highly recommended to **use only Python 3** today. Almost all the
    important modules have been already ported to Python 3. Python 2 exists
    only to keep it possible to run old code when it's really necessary. The
    most important science and data analysis modules like `numpy` and `scipy`
    are about to end Python 2 support.
-   On some Linux distributions and Mac OS X still Python 2 is the default.
    Sometimes the `python` command in the shell is a link to either `python2`
    or `python3`. Same stands for `pip`/`pip2`/`pip3`. Check your system
    and be aware where are your `python` and `pip` exacutables and where is
    the `site-packages` or `dist-packages` directory (where the modules
    install).
-   Always know which Python distribution you use and where do you install
    the modules. If you just call `pip install numpy` and then you start
    a Python shell from the Anaconda distribution, don't be surprised if
    `import numpy` gives a `ModuleNotFoundError`. If you are in doubt you can
    find out by `which python` and something like `ls -l /usr/bin/python` and
    similar ways.

### Linux

In Linux distributions you will find up-to-date and well maintained packages
for both Python 2 and 3 and also many modules. One issue is that `pip` and
the distibution's package manager don't know about each other but will
complain if files already exist (because the other package manager installed
them) and won't recognize if a dependency is already installed by the other
manager. Most often I just give the `force` option to overwrite the files.

### Mac OS X

OS X comes with a built-in Python 2. Sometimes this is quite old. Anyways
probably you will want to install an up-to-date Python 3 distribution.
Most convenient is to install a package manager for OS X (most popular is
HomeBrew, another one is MacPorts) and you can use these to install Python 3
and many other modules.

### Windows

Install Python by the provided installer and don't forget to tick the
"include in the path" box. Also you might consider to install cygwin and
git (actually git installer already offers also cygwin). This way you will
have BASH and git which are essential for development.

### pip

`pip` is the most often used package manager for Python. If `pip` does not
come with your installation you can install it by `easy_install pip`. Or
by your operating system's package manager.

### Editor

If you are about to start writing code it is important to have a good text
editor. In Linux usually not a problem as the default ones like `gedit` can
be tuned to be quite good. Personally I use
[Kate from KDE](https://kate-editor.org/). For Mac and Windows you need to
install one, for example
[Notepad++ is popular for Windows](https://notepad-plus-plus.org/download/v7.5.8.html),
[TextMate is popular for Mac](https://macromates.com/). Also see the IDEs
listed below and you can consider the new
[JupyterLab](https://blog.jupyter.org/jupyterlab-is-ready-for-users-5a6f039b8906)
which is and IDE in the web browser.

### Anaconda

[Anaconda](https://www.anaconda.com/) is a Python and R distribution and
package manager for science and data analysis. They promise standardized
packege management which make collaboration and deployment easier.
Some people like it, I've never used it. For me `pip` and the system's
package manager have been always easy to use and sufficient.

## Where to start?

-   https://www.python.org/ - The home of Python
-   http://stackoverflow.com/documentation/python/topics - In 2016
    StackOverflow started their Documentation project, which aims to be
    a community developed schoolbook and knowledgebase. This rapidly
    developed to one of the best Python learning resources on the web.
-   https://www.codecademy.com/learn/python - Interactive platform to
    learn Python (as well as many other languages). Start here if you
    have never wrote code before.
-   https://www.youtube.com/watch?v=HBxCHonP6Ro&list=PL6gx4Cwl9DGAcbMi1sH6oAMk4JHw91mC\_ -
    Long Python video tutorial for the very beginners
-   https://github.com/mshang/python-elevator-challenge - Beginner
    tutorial with programming an elevator in Python

## Non Python specific but important resources

-   http://stackoverflow.com/ - This very important resource worths
    special mention. As you will se if you google for any programming
    issue, in 90% you will end up on this site. SO is a Q&A (question
    and answer) site where anybody can ask programming related questions
    and answer or comment others questions. Users collect reputation
    points for their contributions which made it a very efficient
    platform for community building around mutual help. Your question
    likely will be answered very quickly, but be careful not to ask
    something already answered by answers for other questions.
-   https://bitbucket.org/ - We suggest you to familiarize yourself as
    soon as possible with version control frameworks. Nowdays the most
    popular is **git**. Version control helps you to keep track of
    changes, keep your project files in order, backup your work often,
    avoid data loss, to collaborate and to share your code in a standard
    and convenient way. BitBucket allows you to to create more private
    repos than the most well known git server,
    [http://github.com/](github.com).
-   https://maryrosecook.com/blog/post/git-from-the-inside-out - If you
    write code please start using git. Sooner is better, even your
    random exercises you can commit to a git repo. Here is an in depth
    introduction to git starting from the basics from Mary Rose Cook.

## Interactive Python learning platforms

-   https://www.codecademy.com/learn/python - Interactive platform to
    learn Python (as well as many other languages)
-   http://www.learnpython.org/ - Lots of tutorials from the basics
-   https://www.datacamp.com/courses/intro-to-python-for-data-science -
    Interactive tutorial focusing on Data Science applications
-   https://www.datacamp.com/courses/intermediate-python-for-data-science -
    Interactive tutorial focusing on visualization with matplotlib

## Programming exercises

When you write code with the aim of learning it is often difficult to
find a task, you want to code, but don't know what to code. In Euler
Problems you find hundreds of small mathematics problems, each of them
you can solve just in a few lines of code, ideal even if you have only
half hour for practicing. As you develop you can return to already
solved problems, and find out better and nicer implementations.
-   https://projecteuler.net/archives
-   http://www.ling.gu.se/~lager/python_exercises.html - 46 very simple
    exercises for completely beginners
-   http://rosalind.info/ - Learning bioinformatics by problem solving:
    a structured repository of bioinformatics problems; you can earn
    badges and reputation by solving these problems

## Python tutorials

-   https://imgur.com/WRuJV6r - Debugging workflow for beginners
-   https://automatetheboringstuff.com/ - Python for beginners, a
    different way, with many tutorials
-   http://www.jessicayung.com/ - Many articles about Python basic topics
    and machine learning, good style, concise but still in-depth information,
    by Jessica Young.
-   https://realpython.com/ - Good and thorough tutorials both for
    beginners and more advanced Python users.
-   http://python.swaroopch.com/ - Learn Python from the beginning by
    tutorials
-   https://www.codementor.io/python/tutorial - Useful tutorials from
    experts
-   https://github.com/faif/python-patterns - Programming patterns in
    Python
-   http://www.python-course.eu/ - A full Python course for beginners,
    covering all important basic topics
-   https://maryrosecook.com/blog/post/a-practical-introduction-to-functional-programming -
    This is a very nice introduction to functional programming in
    Python from Mary Rose Cook.
-   https://chrisalbon.com/ - A massive collection of tutorials
    from Chris Albon, covering statistics, data manipulation, machine
    learning, modeling, plotting
-   https://nbviewer.jupyter.org/github/twiecki/CythonGSL/blob/master/examples/cython_gsl_ipythonnb.ipynb -
    Little quick start tutorial from Thomas V. Wiecki about how to boost
    Python performance with including some C code at critical parts.
-   https://rszalski.github.io/magicmethods/ - A comprehensive guide for
    magic methods from Rafe Kettler. Very helpful when you design your
    classes.

## Python resources

Here we list blogs and essays which are not primarily tutorials, but
give an introduction or insight into specific topics.

-   https://julien.danjou.info/blog/tags/Python - Python related articles
    from Julien Danjou's blog. You can find excellent pieces here, for
    example about testing, profiling, exception handling, pep8 standard,
    etc.
-   https://dbader.org/ - Excellent articles about how Python works
    from Dan Bader.
-   https://jakevdp.github.io/ - Interesting insights into specific
    topics.
-   http://seriously.dontusethiscode.com/ - Nice Python tricks from :james.
-   http://pyvideo.org/ - Thousands of talks from Python conferences
    about a wide range of topics.
-   http://xahlee.info/ - Webpage of Xah Lee, with a huge collection of
    tutorials and opinion articles on programming.

## Online Courses

-   https://www.coursera.org/specializations/python - A Coursera
    specialization for learning Python

## Python environments

-   http://www.bpython-interpreter.org/ - Nice, colorful command line
    environment with smart autocompletion and built in help functions.
-   https://gist.github.com/lonetwin/5902720 - You can easily customize
    your Python shell with editing your **~/.pythonrc*-   file. For
    example, copy the one in this git repo into yours, and you will have
    a colored shell with autocompletion.
-   https://www.pythonanywhere.com/ - A full Python environment in the
    cloud with lots of
    [libraries](https://www.pythonanywhere.com/batteries_included/) and
    many Python versions available. You can write Python scripts in the
    browser, and even deploy your application as a webpage. Free plan is
    available.
-   https://jupyter.org/ - Interactive Python environment in the
    browser: Python runs in the background on your machine, and you
    write the code and get the output in the browser, in so called
    notebooks. Note: formerly known as IPython, they just renamed
    when it became language agnostic (originally it was only for Python,
    but now can be used also with other languages, for example R).
-   https://blog.jupyter.org/jupyterlab-is-ready-for-users-5a6f039b8906 -
    A complete IDE developed from Jupyter.
-   https://www.continuum.io/why-anaconda - Python environment intended
    for science and data analysis, with easy availability of relevant
    modules (at least in theory: eventually installation might be more
    complicated).

## Python modules for data analysis

-   http://www.numpy.org/ - Efficient operations on
    multidimensional numeric arrays (i.e. matrices of numbers).
-   https://www.scipy.org/ - Collection of many stats and science
    methods, like regression, statistical tests.
-   http://pandas.pydata.org/ - Built on top of numpy, pandas provides a
    more convenient handling of data tables, i.e. here you can have row
    and column names, methods for convenient rearranging and filtering
    your data. You can imagine a programmable excel sheet, or something
    like data frames in R.
-   https://jupyter.org/ - Interactive Python environment in the
    browser: Python runs in the background on your machine, and you
    write the code and get the output in the browser, in so
    callednotebooks. Note: this is the same as IPython was, they just
    renamed when it became language agnostic (originally it was only for
    Python, but now can be used also with other languages).
-   https://boltons.readthedocs.org/en/latest/ - Many useful tools for
    advanced Python programming

## Python visualization and plotting

We have seen a number of efforts emerging in the past years with the aim to
provide powerful data visualization in Python, so sciencists and data
analysts would not need to be envy of R user colleagues. Perhaps the perfect
ggplot2 or lattice equivalent is still to come (although two very fresh
libraries, Altair and Plotnine are promising), but each of the
frameworks listed below are very good in certain tasks, and of course
have its limitations. Thus, it is difficult to chose a plotting library,
likely you will try more of them.

-   http://matplotlib.org/ - The
    "grandmother of all Python plotting applications", extremely
    customizable, but complex plotting module. Note: you can use matplotlib
    either by its object oriented interface or by the matlab inspired pylab
    interface, be aware of the differences.
-   http://seaborn.pydata.org/ -
    Module built on matplotlib, providing simple methods and nice default
    styles. And you can still access the low level matplotlib interface, in
    case you need it.
-   https://plot.ly/python/ - An easy way to make
    interactive html plots in IPython notebook. Note: it is not obvious from
    their webpage, but you don't need to register even for the free plan to
    use this library locally and generate html plots; you can install by pip
    and use it just like any other module.
-   http://bokeh.pydata.org/en/latest/ - A plot.ly alternative.
-   http://lightning-viz.org/ - Similar to the former two. Note, in Python
    you can run lightning without server, just like the other plotting
    libraries.
-   http://holoviews.org/index.html - Feature rich, data
    driven plotting framework with matplotlib, seaborn and bokeh backends
    and connections to mpld3 and plotly via extensions.
-   http://pygal.org/en/stable/ - Similar to the 2 above, creates
    interactive plots.
-   https://mpld3.github.io/index.html - Here you
    create the plots with matplotlib, and transform them to d3.js objects,
    so they remain interactive in the browser, independently from Python.
-   https://github.com/vega/vega/wiki/Documentation - A generic
    visualization grammar (i.e. a declarative language to describe
    visualizations).
-   https://vega.github.io/vega-lite/ - A simplified
    version of Vega.
-   https://vincent.readthedocs.io/en/latest/ - A tool
    to define plots in Python and translate them to Vega.
-   https://altair-viz.github.io/ - A declarative visualization module for
    Python using Vega in the background.
-   http://vispy.org/gallery.html -
    This creates and renders dynamic visualizations using the graphic card
    of your computer.
-   http://ggplot.yhathq.com/ - An attempt to make the
    famous R ggplot visualization library available in Python. Does not
    provide all the features and exactly the same interface, but still a
    nice library.
-   https://github.com/sirrice/pygg - Provides access to R
    ggplot2 from Python.
-   https://github.com/dgrtwo/gleam - Creates
    interactive visualizations for browser; Python needs to run in the
    background.
-   https://dansaber.wordpress.com/2016/10/02/a-dramatic-tour-through-pythons-data-visualization-landscape-including-ggplot-and-altair/ - 
    An amusing and detailful comparison of matplotlib, pandas, seaborn,
    ggplot and altair, with 5 examples and analysis. If you want to make an
    informed decision about which library to use, don't skip this.
-   http://pbpython.com/visualization-tools-1.html - Another overview of
tools, but with less details and less examples.
-   https://lisacharlotterost.github.io/2016/05/17/one-chart-code/ - A wider
but less detailed comparison.
-   http://matplotlib.org/style\_changes.html - Good material about color
    maps.
-   https://plotnine.readthedocs.io/en/stable/index.html - So far
    the most faithful implementation of ggplot2 in Python. A great
    declarative plotting library.

## Graphs (networks)

-   http://igraph.org/ - Powerful graph analysis package with full
    featured R and Python interface and great visualization module.
-   http://www.data-imaginist.com/2017/Announcing-ggraph/ - A really
    great new module for graph visualization with R ggplot2. It works
    together with igraph: you can use igraph graphs and layouts
    seemlessly.
-   http://sachaepskamp.com/qgraph - Another super R module for graph
    analysis from Sacha Epskamp. It extends igraph with additional layouts and
    methods, and they work together very well.
-   https://bitbucket.org/snippets/deeenes/LjL5R/good-fruchterman-reingold-layout -
    Sometimes it is difficult to plot a graph with nodes evenly spaced
    and avoiding overlaps. Here are some good parameters for the
    Fruchterman Reingold layout using qgraph but the resulted layout can
    be used with igraph (sadly in the recent version of R igraph the
    fr\_layout method does not handle these parameters hence we must
    calculate the layout with qgraph).
-   https://graph-tool.skewed.de/ - A high-performance graph library
    with Python interface.
-   https://networkx.github.io/ - A network analysis module written
    purely in Python, recently with more features and better
    visualization.
-   https://pygraphviz.github.io/ - Python interface for
    [graphviz](http://www.graphviz.org/), the graph visualization
    library known from its greate layout algorithms.
-   http://kateto.net/network-visualization - In depth R network visualization
    tutorial including dynamic, interactive figures and animations, from
    Katya Ognyanova. Is worth to check out other nice materials [on the
    webpage.](http://kateto.net/)

## Alternative network visualizations

-   http://mkweb.bcgsc.ca/linnet/, http://www.hiveplot.net/ - Hive plots
    from Martin Krzywinski: a great alternative to make visible structures
    in large and complex networks
-   http://www.biofabric.org/index.html - Another tool to make visualization
    of complex networks more clear and informative. By William Longabaugh.
-   http://circos.ca/ - A fancy visualization tool from Martin Krzywinski
    to present a connectogram and many other variables in a complex figure.
-   http://circos.ca/documentation/course/ - On the Circos webpage you can
    find a nice course with many complex visualization examples
-   [Arc diagrams](http://www.gastonsanchez.com/visually-enforced/got-plot/how-to/2013/02/02/Arc-Diagrams-in-R-Les-Miserables/)
    from Gaston Sanchez.
-   http://hangingtogether.org/?p=3053 - Sankey diagrams.

## Visualization in general

-   https://graphicsprinciples.github.io/ - General principles of
    visualization in form of a concise cheatsheet.
-   http://circos.ca/ - A fancy visualization tool from Martin Krzywinski
    to present a connectogram and many other variables in a complex figure
-   http://mkweb.bcgsc.ca/brewer/ - Many blog posts, tutorials and
    examples about data visualization from Martin Krzywinski.
-   http://colororacle.org/ - Tool for checking color blind readability
    of figure colors
-   https://personal.sron.nl/~pault/ - Guide for color blind safe
    palettes from Paul Tol. Especially see the
    [tech notes](https://personal.sron.nl/%7Epault/data/colourschemes.pdf)
-   http://colorbrewer2.org/ - Color palettes from Cynthia Brewer. You
    can access these from R using the
    [`RColorBrewer`](https://cran.r-project.org/web/packages/RColorBrewer/)
    package.
-   http://junkcharts.typepad.com/junk_charts/ - Many visualization critics
    by Kaiser Fung: he takes a wrong data visualization and shows how it
    could be done better
-   http://serialmentor.com/dataviz/ - Excellent free book about basic
    questions of visualization from Claus O Wilke.

## Other tools for graphics and typography: post processing figures, designing slides, posters and figures, typesetting reports, papers, theses and books

-   http://inkscape.org/ - Inkscape is a professional vector graphics
    editor and a free alternative of Adobe Illustrator. Its default
    format is standard SVG, while you can import and export many other
    formats, for example, of course PDF. Of note, you really should not
    pay \$240 per year for an application to a company only to design
    vector graphics. Nor should you make your institute pay it for you.
    This way you only chain yourself to Adobe and the more time and
    energy you invest in learning to use this sophisticated application
    it just constrain you to keep using it and keep paying for it.
    What's the point in this when an excellent free and open source
    alternative is available? Inkscape is powerful and what you learn
    and achieve using Inkscape remains yours forever.
-   http://gimp.org/ - GIMP stands for GNU Image Manipulation Program.
    Is a professional bitmap graphics editor and a free alternative of
    Adobe Photoshop. What I wrote about Inkscape and Illustrator as
    alternatives completely stands also for GIMP and Photoshop.
-   https://www.latex-project.org/ - LaTeX is the best tool and the
    state of the art standard for scientific typesetting and publishing.
    Created in the 80s by Leslie Lamport, and developed by the
    scientific community with the aim of having a tool which completely
    fits their needs. LaTeX is a free and open source software built on
    top of TeX which has been created by Donald Knuth also addressing
    the needs of scientific typography. The difference is that TeX does
    very basic elementary things in the background, like how to fill a
    line of text with symbols, while LaTeX provides macros for more
    complex tasks, like how to size and position items of a list or
    titles on a page in order to make it look good. I can not say LaTeX
    is an alternative of Adobe InDesign, but for scientific publishing
    it is definitely superior. You can of course use it for typesetting
    fiction books or entertaining journals, but maybe you will have more
    difficulties and if you just want an open source alternative for
    this, there is [Scribus](https://www.scribus.net/). If you need help
    with LaTeX don't go to [StackOverflow](https://stackoverflow.com/)
    but to [its sister site dedicated for
    LaTeX](https://tex.stackexchange.com/). One more important thing:
    you can not simply download and install LaTeX, it comes packaged in
    many different distributions, including different fonts, typesetting
    engines and macro packages. First you should look up which of these
    are available for your operating system. And many templates and
    styles are also available, for example journals used to have their
    own article style, universities their own presentation and thesis
    styles.
-   http://www.texample.net/tikz/examples/ - PGF/TikZ is a LaTeX package
    for creating high quality scientific graphics authored by Till
    Tantau. To find out what kind of graphics, see [the examples in the
    galery](http://www.texample.net/tikz/examples/). If your figure
    involves lots of maths, algebra or needs many alignements and
    positioning TikZ might be useful for you. It is worths to take a
    look on the 1161 pages [user manual of
    TikZ](http://mirrors.ctan.org/graphics/pgf/base/doc/pgfmanual.pdf),
    it is really amazing! Or you can start with the [short
    introduction](http://cremeronline.com/LaTeX/minimaltikz.pdf).
-   https://www.wikiwand.com/en/Beamer\_%28LaTeX%29 - Beamer is a LaTeX
    package for creating presentations. In my opinion for scientific
    presentations it is much better than PowerPoint and Keynote which
    are the most awful applications I have ever seen and I am really
    happy I could completely avoid them in the last 15 years. Also
    Beamer is a free and open source software. Most of the default
    themes look not very nice and old-style, but you can easily modify
    them to have something better looking. See examples
    [here](http://heather.cs.ucdavis.edu/~matloff/beamer.html),
    [here](https://sites.google.com/a/wfu.edu/stevenwicker/tech-resources/latex),
    [here](http://deic.uab.es/~iblanes/beamer_gallery/index.html),
    [here](http://www2.informatik.uni-freiburg.de/~frank/ENG/latex-course/latex-course-3/latex-course-3_en.html),
    [here](http://www.cs.ru.nl/~pim/beamer.php),
    [here](https://www.tjansson.dk/2008/01/presentations-with-latex-beamer-class-ku-style/),
    [here](http://hamaluik.com/posts/better-beamer-themes/) or
    [here](https://github.com/matze/mtheme). If you work at EMBL or in
    the Saez-Rodriguez Group at RWTH Aachen University you can find my
    Beamer theme, slightly modified from PaloAlto, in my git repos
    there: [@EMBL](https://git.embl.de/turei/embl-graphics) or
    [@Aachen](https://github.com/saezlab/graphics). Other notes: the
    final format of your slides will be PDF which is perfectly
    cross-platform. You should check or ask the tech support for the
    aspect ratio of the projector in your lecture room. Prepare
    wide-screen (16:9 or 16:10) slides if those fit as you can have more
    space this way. Also check if your connection can transmit this
    resolution and have an HDMI cable and adapter with you if necessary.
    VGA cables are sometimes limited to 4:3 aspect ratio and 1024x768
    resolution which is quite poor.
-   http://www.texstudio.org/ - TeXstudio is a great editor for LaTeX.
    It comes with autocompletion, built in help, embedded compilation
    tool, PDF viewer and many other handy tools.
-   http://gpick.org/ - Gpick is a nice little color picker and palette
    editor application for Linux by Albertas Vyšniauskas. I use it with
    great satisfaction to create palettes what I use later in R, Python,
    Inkscape, GIMP or whereever else. I don't know about alternatives
    for Mac or Windows but definitely there are.
-   https://lvdmaaten.github.io/tsne/ - Dimensionality reduction method
    for 2D/3D visualization.
-   https://distill.pub/2016/misread-tsne/ - Interactive insigths into
    parameter sensitivity and artefacts in the t-SNE dimensionality
    reduction method.

## R blogs and tutorials

-   https://www.rstudio.com/resources/cheatsheets/ - Very helpful and
    concise cheatsheets covering ggplot2, dplyr and some other topics.
    Have them on your desk printed!
-   https://monashbioinformaticsplatform.github.io/r-more/ -
    Introduction to best practices, among others tidyverse
-   https://trinkerrstuff.wordpress.com/
-   https://www.r-bloggers.com/
-   https://kevinushey.github.io/blog/ - In depth articles on many R topics
    including Rcpp from Kevin Ushley, an RStudio developer.
-   https://rpubs.com/bradleyboehmke/data_wrangling - It is not easy to
    understand how `tidyr`'s `gather` works. Here Brad Boehmke explains
    it with visual help.
-   https://www.zevross.com/blog/ - Technical blog from Zev Ross, a
    professional GIS data analyst, many fantastic tutorials not only
    GIS related.
-   https://sebastiansauer.github.io/
-   https://blog.exploratory.io/
-   http://adolfoalvarez.cl/the-hitchhikers-guide-to-the-hadleyverse/ -
    A brief overview of all R packages authored by Hadley Wickham.
-   https://www.tidyverse.org/ - Not only the very nice and comprehensive
    documentation of ggplot2, dplyr and other related packages from
    Hadley Wickham, but many articles and other resources.
-   http://adv-r.had.co.nz/ - If you want to go really pro with R read
    this fantastic free online book with many examples from Hadley
    Wickham.
-   [Viridis color palettes for R](https://cran.r-project.org/web/packages/viridis/vignettes/intro-to-viridis.html)
-   http://www.win-vector.com/blog/ - Interesting insights into many topics
    in R data analysis from Nina Zumel and John Mount. They also have a nice
    book, see below at [R books](#r-books).
-   http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html -
    Selva Prabhakaran
-   http://stat545.com/ - Webpage of the University of British Columbia
    Statistics course. Very good materials most of them with R.
-   https://rpubs.com/ - A page designed for publishing R tutorials. You often
    find here very nice ones by google, but I could not find any index or
    catalogue on the webpage itself, you see the recent ones by default which
    are not guaranteed to be the best ones.
-   https://sebastiansauer.github.io/ - Dozens of great R tutorials, posts
    about statistics and tidyverse from Sebastian Sauer.
-   http://www.listendata.com/ - Tutorials and learning materials for R, Python,
    data analysis and statistics from Deepanshu Bhalla
-   https://martinsbioblogg.wordpress.com/ - Many posts with good R examples
    in Martin Johnsson's bioinformatics blog
-   http://mqasim.me/
-   http://www.sthda.com/english/ - Statistical Tools for High-throughput
    Data Analysis from Alboukadel Kassambara. Many excellent materials mostly
    about R.
-   http://www.brodrigues.co/ - Great posts about statistics and various R
    packages from Bruno Rodrigues.
-   http://colinfay.me/ - Colin Fay's webpage with fantastic R tutorials, many
    insights in numerous topics.
-   https://edwinth.github.io/ - Some really nice tutorials from Edwin Thoen,
    among others about NSE and tidyeval.
-   http://www.gastonsanchez.com/ - A generic introduction to data analysis
    from Gaston Sanchez, not only R but bash, git, makefile, etc.
-   https://nsaunders.wordpress.com/blog/ - Data analysis and bioinformatics
    blog from Neil Saunders: mostly visualization and R.
-   http://cfss.uchicago.edu/syllabus.html - Computing for the Social Sciences
    course University of Chicago. Materials for many topics in R.
-   https://tjmahr.github.io/year-archive/ - Tristan Mahr's professional blog
    with many R related posts.
-   http://cyclismo.org/tutorial/R/ - A comprehensive R tutorial from Kelly
    Black, University of Georgia. You may find also a Matlab tutorial if you
    are interested.
-   https://deanattali.com/ - About shiny from Dean Attali.
-   https://urbaninstitute.github.io/urban_R_theme/ - Nice and clear ggplot
    theme.

## Statistics

These are not Python related but generic.

-   http://simplystatistics.org/ - Nice blog from statistics teachers of
    John Hopkins University and Harvard University 
-   http://varianceexplained.org/ - Another nice blog from data sciencist
    David Robinson
-   http://www.data-imaginist.com/ - Webpage of data
    analyst Thomas Lin Pedersen, author of ggraph. 
-   http://sachaepskamp.com/ - Webpage of Sacha Epskamp, author of qgraph.
    Some good tutorials and a nice dissertation. 
-   http://www.traag.net/ -
    Webpage of Vincent A Traag, who made available louvain community
    detection for Python igraph, plus some other tutorials.
-   http://www.statsblogs.com/ - Blog about statistics, not only R, but
    still many R examples and also visualizations.
-   http://biostat.mc.vanderbilt.edu/wiki/Main/ClinStat - Big collection
    of excellent resources from Frank Herrel, professor of biostatistics
    at Vanderbilt University.
-   https://www.datascience.com/blog/introduction-to-bayesian-inference-learn-data-science-tutorials -
    Simple Bayesian inference example in Python.

### P-values

-   https://amstat.tandfonline.com/doi/pdf/10.1080/00031305.2016.1154108?needAccess=true

#### Debate in Nature Methods

-   http://moscow.sci-hub.tw/e0e621b86fe721cd05bcb08dee2be99a/halsey2015.pdf#view=FitH
    The fickle p-value generates irreproducible results
-   http://twin.sci-hub.tw/6071c3e7dc16d3f300e65737a2b8092d/huber2016.pdf#view=FitH -
    A clash of cultures in discussions of the p-value
-   http://twin.sci-hub.tw/63eed7b3a3c7a2c498bc0d634a94c65a/10.1038@nmeth.3932.pdf#view=FitH -
    Confidence intervals are no salvation from the alleged fickleness of
    the p-value
-   http://twin.sci-hub.tw/e7c2de4af02893f042d4ef126e38f107/halsey2016.pdf#view=FitH -
    Response to: Confidence intervals are no salvation from the alleged
    fickleness of the p-value

#### Others

-   https://www.tandfonline.com/doi/pdf/10.1080/01621459.2017.1289846?needAccess=true
-   http://fivethirtyeight.com/features/statisticians-found-one-thing-they-can-agree-on-its-time-to-stop-misusing-p-values/
-   https://www.youtube.com/watch?v=ez4DgdurRPg - Simulation of p-values
    accross replicates of the same experiment.
-   https://www.nature.com/news/one-size-fits-all-threshold-for-p-values-under-fire-1.22625
-   https://www.nature.com/news/scientific-method-statistical-errors-1.14700
-   https://www.nature.com/news/psychology-journal-bans-p-values-1.17001
-   https://www.nature.com/news/statistics-p-values-are-just-the-tip-of-the-iceberg-1.17412
-   http://shiny-eio.upc.edu/bne/efectos2/
-   https://repository.upenn.edu/cgi/viewcontent.cgi?article=1054&context=marketing_papers

#### Suggestions for new p-value

-   http://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0188299&type=printable
-   https://www.vox.com/science-and-health/2017/7/31/16021654/p-values-statistical-significance-redefine-0005
-   https://www.r-bloggers.com/why-the-ban-on-p-values-and-what-now/
-   http://journals.sagepub.com/doi/pdf/10.1177/0956797613504966

## IDEs (integrated development environments)

IDEs help you to keep track of files in your project, their history,
dependencies, testing, outputs, etc.

### Python IDEs

-   https://www.pythonanywhere.com/ - A full Python environment in the cloud
    with lots of [libraries](https://www.pythonanywhere.com/batteries_included/)
    and many Python versions available. You can write Python scripts in the
    browser, and even deploy your application as a webpage. Free plan is
    available.
-   https://www.yhat.com/products/rodeo - Python IDE similar to RStudio,
    focusing on data analysis.
-   https://www.jetbrains.com/pycharm/ - One of
    the best IDEs for python, with many tools and complex interface 
-   https://www.continuum.io/why-anaconda - Python environment intended for
    science and data analysis, with easy availability of relevant modules

### R IDEs

-   http://rstudio.com/ - Very popular and powerful IDE for R. Built in
    editor, file browser, shell, plot viewer, manual and many other
    helpful tools.

## Image processing

In biology computational analysis of images is often unavoidable. With
high-throughput microscopy you can acquire hundreds of images just in
one hour of time and obviously you can not do all the adjustments and
measurements by hand. Luckily there are a number of easy to use tools
around. You can identify structures and make measurements and finally
come to quantitative data from images. ImageJ is very popular and can
be programmed by its own macro language or many other languages including
Python. But if you want to use Python maybe better to go for Python
image processing modules like scikit-image, OpenCV or ITK.

-   [A comprehensive Introduction from Justin Bois](
    https://justinbois.github.io/bootcamp/2017/lessons/l38_intro_to_image_processing.html);
    check out also the following 2 lessons
-   [Segmentation tutorial 1](https://sbrisard.github.io/posts/20150930-Orientation_correlations_among_rice_grains-06.html)
-   [Segmentation tutorial 2](https://emmanuelle.github.io/a-tutorial-on-segmentation.html)
-   http://scikit-image.org/docs/dev/auto_examples/ - Comprehensive
    scikit-image tutorial.
-   https://opencv.org/ - Open Computer Vision: a great library for image
    and video processing. You can use it in Python but also in C++ or Java.

## Chemistry

-   http://ctr.wikia.com/wiki/Chemistry_Toolkit_Rosetta_Wiki - Chemistry
    software toolkits compared by examples shown side-by-side.
-   http://openbabel.org/wiki/Main_Page - A great chemistry toolkit with C++
    core library and Python interface.
-   http://www.rdkit.org/docs/Overview.html - Also with C++ core, Python
    bindings and integration with many other tools.
-   http://users.abo.fi/mivainio/balloon/ - Nice standalone application for
    2D -> 3D structure prediction. (You can do this with any big toolkit,
    but if you need only this functionality I can recommend.)
-   http://www.openms.de/ - OpenMS is a feature rich high performance mass
    spectrometry and proteomics data analysis toolkit. It comes with Python
    bindings.

## Books

### Python beginner and intermediate books

-   https://automatetheboringstuff.com/ - Python for beginners, a
    different way, with many tutorials
-   http://docs.quantifiedcode.com/python-anti-patterns/ - How NOT to
    use Python. Advanced level
-   https://thehackerguidetopython.com/ - A very nice book both for
    beginners and advanced Python coders. Hint: subscribe for the free
    chapter on the webpage, and you will get weekly mail with
    interesting and very useful blog posts from Julien.
-   http://file.allitebooks.com/20160830/Python%203%20Object-Oriented%20Programming,%20Second%20Edition.pdf -
    In depth material for object oriented programming in Python.
-   https://github.com/jakevdp/PythonDataScienceHandbook - Data science
    book freely available as IPython notebooks. From Jake VanderPlas.

### Advanced Python

-   http://www.effectivepython.com/
-   http://shop.oreilly.com/product/0636920032519.do
-   http://learnpythonthehardway.org/book/
-   http://book.pythontips.com/en/latest/
-   http://www.obeythetestinggoat.com/ - Python testing
-   https://stackoverflow.com/questions/101268/hidden-features-of-python -
    Nice collection of small Python tricks
-   https://docs.quantifiedcode.com/python-anti-patterns/index.html -
    List of bad practices in Python

### R books

-   http://r4ds.had.co.nz/introduction.html - Greate book from Garret
    Gloremund and Hadley Wickham covering many aspects of data analysis
    workflows.
-   http://pdf.th7.cn/down/files/1502/Practical%20Data%20Science%20with%20R.pdf - 
    Practical Data Science with R by Nina Zumel and John Mount

## Lectures

-   https://www.youtube.com/watch?v=2NSbuKFYyvc

## Podcasts

-   https://talkpython.fm/
-   http://podcastinit.com/
-   http://frompythonimportpodcast.com/

## Miscellanous

-   http://pythontips.com/2016/02/27/learning-python-for-data-science/
-   http://pep8.org/ - Standard coding style guide. You will be expected
    to follow these simple rules in any serious project, so better to
    familiarize yourself from the beginning. Tools are available to
    autocheck and in limited cases autocorrect pep8 violations:
    https://flake8.pycqa.org/en/latest/,
    https://fangpenlin.com/posts/2014/02/05/auto-post-commit-pep8-correction/

## Regular expression resources

In data analysis we process tremendous amount of data which is sometimes
noisy and we need to extract information from messy patterns. Regular
expressions sooner or later will be your essential tools no matter which
field and language do you work with. Here are a few excellent resources
to learn these small tricky things called regex:
-   http://rexegg.com/ -
    great, detailful tutorials from beginner to advanced, often with
    interactive demo.
-   http://regular-expressions.info/ - maybe the most
    well known regex page, clear and concise.
-   http://lucumr.pocoo.org/2015/11/18/pythons-hidden-re-gems/ - about
    Python's regex module.

### sed, awk, grep

-   http://www.catonmat.net/series/sed-one-liners-explained - Good resource
    for learning `sed` (the *s*tream *ed*itor, a swiss army knife of the Unix
    shell). From Peter Krumin.
-   http://www.catonmat.net/blog/awk-one-liners-explained-part-one/ - `awk`
    one liners explained: `awk` is another poweful "swiss army knife" of the
    Unix shell. This guide is as good as the one about `sed`, also from Peter
    Krumin. `awk` got its name from the initials of its original authors:
    Alfred Aho, Peter Weinberg and Brian Kernighan.
