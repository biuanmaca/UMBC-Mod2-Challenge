# VBA Challenge -- Selected Stock Analysis

## Overview of Project

A basic analysis of a selection of stocks with refactored code to improve performance.

### Purpose
In order to select a performing stock, a selection of stocks are compared showing their individual trade volumes
and their performance percentage for that year.  The two years being looked at are 2017 and 2018.  The selection 
of stocks are as follows:  AY, CSIQ, DQ, ENPH, FSLR, HASI, JKS, RUN, SEDG, SPWR, TERP, VSLR

## Analysis and Challenges

### Analysis of Outcomes Original Code

The original code successfully pulled all the data from the raw stock information and outputted the volumes and 
the performance percentage for the user designated year for each separate ticker.  To do this, the code made use 
of nested FOR loops and looping through all the data for each ticker.  Efficiency the code was suboptimal, being 
that it took 1.05 secs to process.  

![OldCodeSpeed](https://user-images.githubusercontent.com/91292960/136719789-0befd811-0bbe-4c83-88ae-96a55b3f45ff.png)

### Analysis of Outcomes Based on Goals

The refactored code peformed the same output: namely the volumes and the performance percentage for the user 
designated year for each separate ticker.  Instead of the nested FOR loops which required the processor to loop
through all of the data 12 times, the refactored code made use of 2-dimensional arrays in order to capture all
the information in a single pass through the data.  This greatly improved efficiency of the code, though the
now deprecated code remains for reference purposes.  The new processing time comes out to 0.24 secs.

![RefactoredCodeSpeed](https://user-images.githubusercontent.com/91292960/136720062-52712868-6c88-4f39-957c-826ee030dfd1.png)

## Summary

The refactored code greatly improved the performance of the code.  For such a small data set, this improvement,
though noticeable, was not necessary as the speed of the old code was acceptable.  The old code however is
easier to follow and less complicated in some ways.

Since the original code would be slowed further and further the larger the data set were to become or the 
larger the number of stocks in the selection (therefore increasing the number of times the code needed to loop
through all the data), scaling this up would quickly create a performace that was grossly unsatisfactory and
the refactored code would be absolutely needed.

## Results

The original aim was to compare and contrast the selection of stocks to determine the best stock to choose.
There was an opening preference for ticker DQ.  The data shows that while in 2017 it was the best performer
of the selection of stocks, in 2018 it was the worst performer.  This indicates that this stock may have 
high volatility and may not be the best stock for risk-averse individuals.  The best performing stock in 2018
was RUN, but in 2017 it was the 2nd worst performer.  That said, unlike DQ both results for RUN were positive
indicating that for the same volitility, RUN may be a preferred choice.

There are limitations with this analysis, however, and more analysis is recommended.  For one, the scope is
pretty small (only twelve stocks).  Broadening the selection of the analysis would improve the chances of 
picking a performing stock, though a all-market analysis may not be practical.  It would also be advisable
to bring in more data to show at minimum a 5-year trend but preferably a 10-year trend.  That all said, please
remember the financial advisor mantra:  past performance does not guarantee future gains.
