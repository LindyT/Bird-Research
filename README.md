# Bird-Research
Code used for analysing data, calculating home-ranges, and creating graphs.

Suggested citation: Thompson, L.J. (2020) Breakpoint regression for monthly home-range. DOI: 10.5281/zenodo.3743276

My research question: 
What is the minimum number of months one must track a bird to get a reliable estimate of its home-range size?

The code presented is for a model that included ‘Subspecies’, ‘AgeClass’, ‘Sex’ and ‘MonthOfStudy’ as fixed effects,
with piecewise regression for ‘MonthOfStudy’ 
and with ‘BirdID’ as a random factor (various months of data were used from the same birds),
in the example below we also included ‘DutyCycle’ and ‘No_fixes_Monthly’ as fixed effects, 
to account for the variation in Duty Cycles of birds’ tracking units, 
and to account for the fact that some birds had more fixes per month than other birds.

First, you need to calculate home-range size for each cumulative month of your data,
i.e. just month 1, then just months 1 and 2, then just months 1, 2 and 3, all the way up to just months 1 to n, 
where n is the total number of months the bird was tracked for. 
