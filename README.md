# Julia-for-HPC

[![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](<https://praksharma.github.io/Julia-for-HPC/>)

The repo contains docs for using Julia with HPC for machine learning.

## Jupyter-book
The doc is created using [Jupyter-book](https://jupyterbook.org/en/stable/intro.html).

### Setting up Jupyter-books
These steps will allows you to create a basic setup. For more details visit [here](https://jupyterbook.org/en/stable/start/your-first-book.html). 
1. Create a new Python virtual environment.

```sh
python3 -m venv jupyter_env
```

2. Install Jupyter-book.
```sh
pip3 install -U jupyter-book
```

3. Create a template for quick start.
```sh
jupyter-book create docs/
```
This will create a directory in the ```$PWD``` named ```docs/```. The table of contents are stored in ```_toc.yml``` and the configuration is stored in ```_config.yml```.

4. Building a project

```
jupyter-book build docs/
```

For a full rebuild:

```
jupyter-book build --all docs/
```

If the toc doesn't update. This will update the entire project.

5. Publish the docs in the new branch

```
ghp-import -n -p -f docs/_build/html
```

6. Deploy website
Go to "Settings->Pages" of the repo. Set the "Source" to "Deploy from a branch". In the "Branch", select the "gh-pages" branch and location as the "/root".

7. GitHub pages force build
GitHub pages is known for its laziness. To force deploy the website go to "Setting->Pages". Here, search for the following line:

> Your site was last deployed to the github-pages environment by the pages build and deployment workflow.

Click on "pages build and deployment" and click on the button "Re-run all jobs" on the top right corner.

## Julia kernel and Jupyter books
It is really tricky to compile notebooks written in Julia. One of my homie created [this](https://compwa-org.readthedocs.io/develop.html#ijulia-notebooks) nice docs for us. 

