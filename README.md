# HUNT Cloud internal wiki
This is internal documentation and guiding principles for how the CIMORe group uses the HUNT Cloud platform. It is meant as a reference document to ensure common practices.

This documentation is markdown-based. To suggest a change or addition, edit or add a new markdown file to the [`docs`](docs) folder. The repository is set up with github actions to automatically rebuild after a new commit to the main branch. If a new markdown file is added, make sure to add it to the `nav` in the [mkdocs.yml](mkdocs.yml) file.

## Extensions
We try to stick to fairly standard markdown to keep the documentation portable. See the [mkdocs.yml](mkdocs.yml) file for the extensions we are currently using. Currently only the  [admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) extension is in use.

## Advanced edits
This documentation is build using the [Material theme](https://squidfunk.github.io/mkdocs-material/) for [MkDocs](https://www.mkdocs.org/). Please refer to the documentation for the [Material theme](https://squidfunk.github.io/mkdocs-material/getting-started/) if you want to make more advanced edits to the documentation. In this case, make sure to host the page locally to make sure that the modifications works as intended before pushing to github.