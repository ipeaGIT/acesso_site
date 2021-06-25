if (file.exists('~/.Rprofile')) sys.source('~/.Rprofile', envir = environment())

# load some packages and functions at startup in a project
library(blogdown)
library(processx)
library(later)


options(
  digits = 4, formatR.indent = 2, expressions=10000,
  blogdown.author = NULL, 
  # blogdown.generator.server = TRUE,
  blogdown.hugo.server = c('-D', '-F', '--navigateToChanged'),
  blogdown.hugo.version = "0.84.1"
)
