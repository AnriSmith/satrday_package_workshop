SCHEDULE
=========================================================

# Session 1

* Check everyone's installations... in the worst case pair people.

* Intro slides about why to learn about package development, and about automation.

* Make usethis and devtools available

if (interactive()) {
  suppressMessages(require(devtools))
  suppressMessages(require(usethis))
}

* Create package skeleton
usethis::create_package
modify DESCRIPTION
usethis:: licence

* Create and document a first function
create give_age, load_all 
then write documentation of that function
change project options roxygen2
show NAMESPACE et man

* Install the package

install package and show it's there in the library

* git and GitHub setup
use_git_config(user.name = "Jane Doe", user.email = "jane@example.com")
use_git

create repo GitHub
clone it
push


Yes I'd like to have the GitHub repo set up right from the beginning
This way one can commit and navigate to the repo
which is a way to take a break and to see what's just been done
Plus, it's best practice.

* Create the package doc if time allows
use_package_doc

# Session 2

* First unit test
use_testthat, use_test

* Create the praise function that uses two external packages
praise&magrittr
importFrom
ou ::
use_package

* Create the give_name function that uses external data
Note that I'll have shared the data but also the code creating it.
data
data-raw
document data, global variable
write about data copyright in licence and DESCRIPTION
create the function itself

So yay now we have 3 functions and we now how to test code!

# Session 3

* devtools::check!
Mention other checks in passing (lintr, spellcheck, goodpractice)/
do them on my laptop telling them not to do that yet (bc otherwise install issues)

* use_travis, use_coverage -- mention use_appveyor

* Give the cheatsheet from RStudio, good way to get questions

* GitHub exploration 
Goal = make the repo discoverable from the package docs
and making it look useful and friendly
use_github_links
use_readme 
use_conduct

depending on time
what does one see on GitHub
Mission: go star the repo of your neighbour
and follow your neighbour
then open an issue in your repository e.g. "add a cool function"
and assign yourself


# Session 4

Show them two things

* vignette, pkgdown.

* package analytics slide

Choose your own adventure
AND take all their questions

* Write a vignette and make a pkgdown website.

* add more tests, functions, etc, as you wish.

* usethis setup

* more checks? suggest them to use lintr, spell_check, goodpractice. 

* trying things out on GitHub e.g. pull requests to each other's packages,
creating branches

* analytics of your favorite packages