# Distortion Sequence Matching
 Code and data supporting the paper "Objectively correct sequence matching for comparing pipeline inspections", AGPL-3.0-or-later



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
