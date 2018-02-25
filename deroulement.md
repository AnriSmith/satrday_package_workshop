Acheter des post-its vert et rouge, enfin de deux couleurs, car il y aura des helpers.

Montrer un exemple de paquet sur Github dont les issues ont des labels (de rOpenSci ou de la tidyverse).

Imprimer la cheatsheet de RStudio de R package development et la distribuer à la fin / avant le dernier créneau.

Réserver le dernier créneau à des questions / trucs moins cruciaux / rattrapage de retard.

Send data and LICENCE for data to everyone

=========================================================

BASICS
if (interactive()) {
  suppressMessages(require(devtools))
  suppressMessages(require(usethis))
}

usethis::create_package
modifier DESCRIPTION
usethis:: licence

delete
usethis options name
options(
  usethis.name = "Maëlle Salmon",
  usethis.description = list(
    `Authors@R` = 'person("Maëlle", "Salmon", email = "maelle.salmon@yahoo.se", role = c("aut", "cre"))',
    License = "MIT + file LICENSE",
    Version = "0.0.0.9000"
  )
)
usethis::create_package


créer fonction give_age, load_all puis documenter
attention project options roxygen2
montrer NAMESPACE et man
installer et montrer que c'est là 
use_pkg doc

use_git_config(user.name = "Jane Doe", user.email = "jane@example.com")
use_git

créer repo GitHub
cloner
push
montrer ce qu'on voit sur Github
mission: go star the repo of your neighbour
and follow your neighbour
then open an issue in your repository e.g. "add a cool function"
and assign yourself
see more details in Jenny's book

liens use_github_links
use_readme et code de conduite

use_testthat, use_test

praise&magrittr
importFrom
ou ::
use_package

data
data-raw
documenter donnéees, global variable
licence et DESCRIPTION

creer fonction

vignette

devtools::check

à ce moment, donner cheatsheet et faire le point et les faire ajouter tests, vignette, liens dans docs etc.
montrer flowchart again

use_travis CI
use_covr
mention use_appveyor

lintr
spell_check
goodpractice

How to install
show how to: NEWS.md + release!

now if time and maybe as choose your own adventure?
- pkgdown
- package analytics
- usethis setup
- trying things out on GitHub e.g. pull requests to each other's packages,
creating branches