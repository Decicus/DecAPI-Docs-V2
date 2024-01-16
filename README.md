# DecAPI Documentation

TODO

## Setup for development

- Requires Python 3.9+, with `python3-venv`
    - Runs just fine on Python 3.11.2 at least
- In the project directory:
    1. Create the virtualenv (aka venv): `python3 -m venv venv`
    2. Load the virtualenv: `source venv/bin/activate`
        - Your shell prompt should now be prefixed with `(venv)`
    3. Once venv is active, install requirements: `pip install -r requirements.txt`
        - To run the development server locally, with auto-reload on changes: `mkdocs serve`
        - To build the documentation for publishing to production: `mkdocs build`
    4. Once you're done working on the docs, deactivate the venv: `deactivate`
        - Your shell prompt should now be back to normal

## Writing documentation for a new endpoint

- Create a new Markdown file in `docs/{parent}/{endpoint-name}.md`
    - Probably a good idea to use an existing endpoint as a template, find one that's similar if possible.
- Add the new endpoint to `mkdocs.yml` under `nav.Documentation`
