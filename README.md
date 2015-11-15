# A syberia modeling project

This repository gives a full example of how to use Syberia
for a modeling project. It consists of the following files:

  * [The lockfile](lockfile.yml) - A specification of which packages
    should be loaded for an R session using this project through
    [lockbox](https://github.com/robertzk/lockbox).
  * [The engines file](config/engines.R) - This file is necessary
    for any Syberia project. In this example, we are using the
    [modeling engine](https://github.com/syberia/modeling.sy).
  * [An example model](models/dev/example1.R) - A trivial model
    showing how to create an [`lm`](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/lm.html)
    classifier with some trivial feature engineering. After running
    this model, the final output will be in a global variable
    called `model`.
  * [An example mungebit](lib/mugnebits/sanitize_gender.R) - A trivial
    [mungebit](https://github.com/robertzk/mungebits2), the Syberia
    approach to feature engineering that allows re-use of the same
    code during experimental sandbox training and real-time prediction.
  
To run the example model, type `run("example1")`. This uses
[fuzzy matching](https://github.com/kien/ctrlp.vim), so you can
run the model by leaving out letters as long as they appear
consecutively in the model filename: `run("ex1")` or `run("mple")` will
work equally well.

