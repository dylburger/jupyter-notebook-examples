This directory provides an example project structure for Python analysis projects.

There is no well-shared convention for how to structure your code into subdirectories. There are a couple of reasons I hypothesize this is the case:

* Analysts are not software developers. In software development, project structures are often built into the tooling (e.g. [Ruby on Rails](https://www.sitepoint.com/a-quick-study-of-the-rails-directory-structure/) or established by convention.
* Analyses may be as small as a Jupyter notebook or contain many shared modules, notebooks, other scripts and applications. You shouldn't impose a structure for unnecessary code, where your use case is simple.

If you have a single Jupyter notebook, you may not need a project structure. As your project grows, consider some of the examples and references below.

### Basic project structure

As your project grows, you may want to impose some structure to help your team know where to find things. In general, a single level of subdirectories at the root of your repository will suffice:

    requirements.txt
    charts/
    data/
    docs/
    modules/
    notebooks/

In this example, I've saved charts and other images to `charts`. Data (CSVs, JSON, etc.) go in `data`. If I have documentation for the project (for instance, larger learnings from the project that don't make sense to keep inline in Jupyter notebooks), that's stored in `docs`. `modules` contain shared Python code I can use across Jupyter notebooks, and `notebooks` contain the notebooks themselves.

The `requirements.txt` file stores the Python modules required to run the code in this project, stored by running

    pip freeze --local > requirements.txt

### Other references

* [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/)
* [Shablona (template for data science projects)](https://github.com/uwescience/shablona)
* [Example project structure](https://github.com/oxananu/data-analysis-sample)
* [Example project structure for an R project](https://medium.com/human-in-a-machine-world/folder-structure-for-data-analysis-62a84949a6ce)
