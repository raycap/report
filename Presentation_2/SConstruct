import os, subprocess

env = Environment(ENV=os.environ)
# Build the paper
env.AppendUnique(PDFLATEXFLAGS='-synctex=1')
filename = 'main'
pdf = env.PDF(filename + '.tex')
# Force to rebuild when the references file changes
dependencies = ['references.bib']
Depends(pdf, dependencies)
# make sure that the pdf is reloaded properly (e.g., in Skim)
env.Precious(pdf)
# Extensions to clean
extensions = ['.synctex.gz', '.bbl', '.blg', '.bcf']
for extension in extensions:
  env.Clean(pdf, filename + extension)
env.Clean(pdf, 'SConstructc')
env.Clean(pdf, '.sconsign.dblite')
env.NoClean(pdf)
