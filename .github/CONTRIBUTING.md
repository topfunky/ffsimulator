# Contributing

Many hands make light work! Here are some ways you can contribute to this project:

### Sponsor
- You can [sponsor this project by donating to help with server costs](https://github.com/sponsors/tanho63)!

### Open an issue

- You can [open an issue](https://github.com/DynastyProcess/ffsimulator/issues/new/choose) if you'd like to request a specific function or report a bug/error.

### Fixing typos

*   You can fix typos, spelling mistakes, or grammatical errors in the documentation directly using the GitHub web interface, as long as the changes are made in the _source_ file. This generally means you'll need to edit [roxygen2 comments](https://roxygen2.r-lib.org/articles/roxygen2.html) in an `.R`, not a `.Rd` file. 
You can find the `.R` file that generates the `.Rd` by reading the comment in the first line.

### Bigger changes

*   If you want to make a bigger change, it's a good idea to first file an issue and make sure someone from the team agrees that it’s needed. If you’ve found a bug, please file an issue that illustrates the bug with a minimal 
[reprex](https://www.tidyverse.org/help/#reprex) (this will also help you write a unit test, if needed).

### Project and branch strategy

*   Feature development for this package is organized with GitHub Projects, each of which track towards a **minor version release**.
*   Each function/method is tracked as a GitHub Issue, and linked to/closed by Pull Requests.
*   The `main` branch contains the code for the current CRAN version of the package.
*   The `dev` branch reflects a fully-tested, linted, and documented version of the proposed release.
*   Feature branches are built off of the dev branch, add function/method + documentation + testing, and then is squash-merged back onto the staging branch once developed. 

### Pull request process

*   Fork the package and clone onto your computer. If you haven't done this before, we recommend using `usethis::create_from_github("dynastyprocess/ffsimulator", fork = TRUE)`.

*   Install all development dependencies with `devtools::install_dev_deps()`, and then make sure the package passes R CMD check by running `devtools::check()`. 
    If R CMD check doesn't pass cleanly, it's a good idea to ask for help before continuing. 
*   Create a Git branch for your pull request (PR). We recommend using `usethis::pr_init("brief-description-of-change")`.

*   Make your changes, commit to git, and then create a PR by running `usethis::pr_push()`, and following the prompts in your browser.
    The title of your PR should briefly describe the change.
    The body of your PR should contain `Fixes #issue-number`.

*  For user-facing changes, add a bullet to the top of `NEWS.md` (i.e. just below the first header). Follow the style described in <https://style.tidyverse.org/news.html>.

### Code style

*   New code should follow the tidyverse [style guide](https://style.tidyverse.org). 
    You can use the [styler](https://CRAN.R-project.org/package=styler) package to apply these styles, but please don't restyle code that has nothing to do with your PR.  

*  We use [roxygen2](https://cran.r-project.org/package=roxygen2), with [Markdown syntax](https://roxygen2.r-lib.org/articles/rd-formatting.html), for documentation.  

*  We use [testthat](https://cran.r-project.org/package=testthat) for unit tests. 
   Contributions with test cases included are easier to accept.  

### Code of Conduct

Please note that the usethis project is released with a
[Contributor Code of Conduct](CODE_OF_CONDUCT.md). By contributing to this
project you agree to abide by its terms.

*These contribution guidelines were inspired by the guidelines from [{usethis}](https://github.com/r-lib/usethis)*
