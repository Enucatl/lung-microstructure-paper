require "rake/clean"

namespace :main do

  desc "main pdf"
  file "main.pdf" => ["main.tex", "bibliography/biblio.bib"] do |f|
    sh "pdflatex main"
    sh "bibtex main"
    sh "pdflatex main"
    sh "pdflatex main"
  end

  CLEAN.include(FileList["*.aux", "*.bbl", "*.blg", "*.brf", "*.idx", "*.ilg", "*.ind", "*.log", "main.pdf"])


end
