# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line.
SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = blotter
SOURCEDIR     = .
BUILDDIR      = _build
GITHUB_REPO=https://github.com/matthewgilbert/blotter.git
GITHUB_PAGES_BRANCH=gh-pages:gh-pages


# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
	@echo
	@echo "and"
	@echo "  github   to push documentation to gh-pages"

.PHONY: github
github:
	ghp-import -m "Sphinx Documentation" $(BUILDDIR)/html
	git push -f $(GITHUB_REPO) $(GITHUB_PAGES_BRANCH)
	@echo
	@echo "Pushing docs to gh-pages on GitHub"

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
