# Distortion Sequence Matching
 Code and data supporting the paper "Distortion-guided sequence matching for comparing pipeline inspections", AGPL-3.0-or-later



### A note on data availability:

Recent news about the bombing of the Nordstream pipeline, as well as other acts of vandalism or terror, should make it clear that pipeline data is extremely sensitive. To that end, we have taken the following steps to obscure the data offered here :

1. We have released a minimal data set to support the induction only. There are only two columns for each event, odometry and event class. 
2. Event class values for reference points have been randomly aggregated. This has reduced the precision of the results that this data can generate since what may have been three different types of reference points, are now represented by only one.
3. The original index values are not included because they imply the amount of corrosion on a joint. This information could be misused.
4. Data for the hybrid method, using semantic Needleman-Wunsch, is too sensitive for release. It requires all columns from the event attribute vector. We are contemplating how to generate a synthetic data set for this.

# Contents

Code is Python in the form of Jupyter notebooks. GitHub has a python notebook viewer builtin.  Click on the files to see the rendered form, complete with graphs.

* `Inductive Algorithm.ipynb` - Inductive algorithm

  * contains some guidance about using code notebooks
  * select from one of the four examples from the paper
  * data is minimal required to make code work -
    *  `odometer` 
    * `event class`
  * RC2 gets lost because there are so many gaps

  

* `Grid Search - RC3.txt` - Grid search for inductive parameters

  * Uses RC3, is close to other examples (except RC2)
  * Tries to optimize results
  * 4.4 sec execution time is > 3 times faster than reported in the paper

  

* `Stationarity - Tests Final.ipynb` - Stationarity tests

  * uses hybrid results from the four examples
    * sets [0,3] are raw output from the NW algorithm
    * sets [4,7] were cleaned using the induction at $p$
  * There are more tests here than were in the paper
    * building a preponderance of evidence
    * demonstrates that Eqn. $(10)$ is correct

# License

(c) October 2022, Craig L Champlin
LICENSE: GNU Affero General Public License v3.0
https://choosealicense.com/licenses/agpl-3.0/
