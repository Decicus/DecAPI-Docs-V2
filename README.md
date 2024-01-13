# DecAPI Documentation

TODO

## Setup for development

- Requires Python 3.9, with `python3-venv`
    - Might work on newer versions, but only tested on 3.9
- In the project directory:
    - `python3 -m venv venv`
    - `source venv/bin/activate`
    - `pip install -r requirements.txt`
- To run the development server locally, with auto-reload on changes:
    - `mkdocs serve`
- To build the documentation for publishing to production:
    - `mkdocs build`

## Writing documentation for a new endpoint

- Create a new Markdown file in `docs/{parent}/{endpoint-name}.md`
    - Probably a good idea to use an existing endpoint as a template, find one that's similar if possible.
- Add the new endpoint to `mkdocs.yml` under `nav.Documentation`
