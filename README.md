# FlightDelays

The dataset below FlightDelays.csv contains information on all commercial flights departing theWashington, DC area and arriving at New York during January 2004. For each flight, there is informationon the departure and arrival airports, the distance of the route, the scheduled time and date of the flight,and so on. The variable that we are trying to predict is whether or not a flight is delayed. A delay isdefined as an arrival that is at least 15 minutes later than scheduled.

In R Your Job is To:
Step 1:
Preprocess the Data:
Transform
variable day of week (DAY_WEEK) info a categorical variable.
Bin
the scheduled departure time into eight bins (in R use function
cut()
).
Use
these and all other columns as predictors (excluding DAY_OF_MONTH).
Partition
the data into training and validation sets.

Step 2:
Once you've preprocessed the data, complete the following:
Fit
a classification tree to the flight delay variable using all the relevant predictors.
Do
not
includeDEP_TIME (actual departure time) in the model because it is unknown at the time of prediction(unless we are generating our predictions of delays after the plane takes off, which is unlikely).
Use
a pruned tree with maximum of 8 levels, setting cp = 0.001. Express the resulting tree as a setof rules.
Tell me:
If you needed to fly between DCA and EWR on a Monday at 7:00 AM, would you be able touse this tree? What other information would you need? Is it available in practice? What information is
redundant? Then:
Fit
the same tree as you did initially, this time excluding the Weather predictor. Display both thepruned and unpruned tree. You will find that the pruned tree contains a single terminal node. Then
tell me:
How is the pruned tree used for classification? (What is the rule for classifying?)
To what is this rule equivalent?
Examine the unpruned tree. What are the top three predictors according to this tree?
Why, technically, does the pruned tree result in a single node?
What is the disadvantage of using the top levels of the unpruned tree as opposed to the prunedtree?
Compare this general result to that from logistic regression in the example in Chapter 10. Whatare possible reasons for the classification tree’s failure to find a good predictive model?
