# STEM Camp: Intro to Machine Learning Notebooks

This repository contains Jupyter Notebooks for the STEM Camp: Introduction to Machine Learning class.

If you haven't come across [Jupyter Notebooks](https://jupyter.org/) before, a Notebook is a web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. In this class, we use Notebooks because their web-based nature makes it easy to get started for new users. The fact that Notebooks run in a web browser also makes it easy to render data visualization in the middle of some calculations. This is useful for learning about the data while doing Machine Learning and it's also useful for telling a story about the data.

## Running Locally

To run these notebooks on your local computer, make sure that you have a working Python installation. You can download the latest version of Python from the [Python Downloads](https://www.python.org/downloads/) page. For example, once you have Python installed, you should be able to run the following command from a terminal and see a similar result (don't worry if you have a slightly different version of Python):

```
$ python --version
Python 3.7.3
```

Now, you must install the application dependencies (like all of the data science and machine learning tools):

```
pip install -r requirements.txt
```

Now you are ready to start the Jupyter Notebook server. To start the Jupyter Notebook, run the following command from the root of this repository:

```
$ jupyter notebook
[I 18:15:09.524 NotebookApp] Serving notebooks from local directory: /stem-camp-notebooks
[I 18:15:09.524 NotebookApp] The Jupyter Notebook is running at:
[I 18:15:09.524 NotebookApp] http://localhost:8888/?token=1f1f576e8efc50878ac1fc0bafd83b2d9a1e8bbcbd46d17f
[I 18:15:09.524 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```

Copy and paste that link into your web browser and you're ready to go! Feel free to navigate to the Notebook you want to view.