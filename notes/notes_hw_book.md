Installation instructions ��
pkgbuild::check_build_tools()
Pandoc

" Don’t use package.skeleton() to create a package"

Will not teach compiled code but say hadley book + rcpp for everyone

I want to get you started, with good automatisms and a nice list of resources to go further

Namespace
- via roxygen2
- export tag
- pkg::fun even if longer and slower
- i will not mention classes but export similar

devtools::use_build_ignore

devtools::load_all() and RStudio’s “Build and reload

" While you’re free to arrange functions into files as you wish, the two extremes are bad: don’t put all functions into one file and don’t put each function into its own separate file."

"You don’t have to use my style, but I strongly recommend that you use a consistent style and you document it
Include link to Hadley's error messages style guide when available"
Donner lien vers tidyverse style guide

Do not modify global settings

" The flip side of the coin is that you should avoid relying on the user’s landscape, which might be different to yours. For example, functions like read.csv() are dangerous because the value of stringsAsFactors argument comes from the global option stringsAsFactors. If you expect it to be TRUE (the default), and the user has set it to be FALSE, your code might fail."

Re find Miles' code that determines the minimal R version

" You can also list things that your package needs outside of R in the SystemRequirements field. But this is just a plain text field and is not automatically checked. Think of it as a quick reference; you’ll also need to include detailed system requirements (and how to install them) in your README"

Describe DESCRIPTION fields incl url + bugreports and lazydata

" The most important thing to note is that your email address (i.e., the address of cre) is the address that CRAN will use to contact you about your package. So make sure you usep an email address that’s likely to be around for a while"

Links to license guides (from the book)

Links between doc pages

Bien config projet pr q la doc soit construite à chaque build

Version numbers 

" ve been careful to wrap the roxygen block so that it’s less than 80 characters wide. You can do that automatically in Rstudio with Ctrl/Cmd + Shift + / (or from the menu, code | re-flow comment)."

" You can add arbitrary sections to the documentation with the @section tag. This is a useful way of breaking a long details section into multiple chunks with useful headings. Section titles should be in sentence case, must be followed by a colon, and they can only be one line long"

" For the purpose of illustration, it’s often useful to include code that causes an error. \dontrun{} allows you to include code in the example that is not run. ("

"Roxygen2 provides two ways to avoid repetition in the source, while still assembling everything into one documentation file:

The ability to reuse parameter documentation with @inheritParams.

The ability to document multiple functions in the same place with @describeIn or @rdname"


Special characters roxygen

Add package level docs

Qq bases de Markdown 
Qq options de RMarkdown chunks

Citer les 4 avantages des unit tests et y ajouter compliment de praise

Montrer des exemples de expect_blabla

" Each test is run in its own environment and is self-contained. However, testthat doesn’t know how to cleanup after actions affect the R landscape:" (verifier q c encore le cas)

Citer l'avis sur comment ecrire tests, et le livre de Richie Cotton

Skip options

Ecrire ses propres fonctions expect

Where to put data 

devtools::use_data et son argument internal

devtools::use_data_raw

" There are two additional tags that are important for documenting datasets:

@format gives an overview of the dataset. For data frames, you should include a definition list that describes each variable. It’s usually a good idea to describe variables’ units here.

@source provides details of where you got the data, often a \url{}.

Never @export a data set."

"You should also make sure that the data has been opt

You should also make sure that the data has been optimally compressed:

Run tools::checkRdaFiles() to determine the best compression for each file.

Re-run devtools::use_data() with compress set to that optimal value. If you’ve lost the code for recreating the files, you can use tools::resaveRdaFiles() to re-save in place

Package CITATION

Commits best practices

From Jenny " Also, alot of people don’t really know where packages live and the different forms a package can take (source vs bundle vs installed). How do you move a package from one form to the next? I certainly did not know this! And somehow I found that necessary to understand before I felt comfortable developing a package."

" R CMD check is composed of over 50 individual checks, described in the following sections. For each check, I briefly describe what it does, what the most common problems are, and how to fix them. When you have a problem with R CMD check and can’t understand how to fix it, use this list to help figure out what you need to do."

" An easy way to install any missing or outdated dependencies is to run devtools::install_deps(dependencies = TRUE)."

" If you need to fix a major bug, be apologetic."

" You can run the most common of these outside devtools::check() with devtools::check_doc()(which automatically calls devtools::document() for you). If you have documentation problems, it’s best to iterate quickly with check_doc(), rather than running the full check each time"

Mention deprecation
Livre et http://bioconductor.org/developers/how-to/deprecation/

devtools::release et cran comments

R hub

Revdep mais bon pas pour premier paquet tout jeune

Allows you to add your own questions to the check process by including an unexported release_questions() function in your package. This should return a character vector of questions to ask. 
