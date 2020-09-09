---
id: 244
title: R Style Guide
date: 2012-09-21T22:59:18-07:00
author: Michael
layout: post
guid: http://www.schulte-mecklenbeck.com/?p=244
permalink: /2012/09/r-style-guide/
categories:
  - Google
  - R
  - Statistics
---
This is mainly a note to self:

There are several style guides for R out there. I particularly like the one from [Google](https://google.github.io/styleguide/Rguide.xml "Google R Style Guide") and the somewhat lighter [version of Hadley](http://stat405.had.co.nz/r-style.html) (ggplot god).

All of that style guide thinking started after a question on <stackoverflow.com> about R workflow &#8230; How do we organize large R projects. Hadley (again) is favoring an Load-Clean-Func-Do approach which looks somewhat like that:

  * load.R # load data
  * clean.R # clean up crap
  * func.R # add functions
  * do.R # do the work

I kind of started doing something along these lines, with splitting files into load/clean (still together, could go separate &#8230;), cleaning, graphing (which does not make a lot of sense in an extra file) and large junks of analysis &#8230; got to redo some directories now &#8230;

Other cool links from today&#8217;s follow-this-link trip: <http://www.getskeleton.com/> and <http://subtlepatterns.com/>