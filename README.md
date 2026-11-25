# ACCESS-NRI Profiling Studies

## About

This repository is a collection of Jupyter Notebooks that profile and benchmark the ACCESS-NRI models. Each notebook is a study of one question about the performance of a model configuration, such as how the layout of its components, the decomposition of a component or the way it is run changes how long it takes. The notebooks generate and run the experiments of the study, and then analyse their profiling data.

The scaling of the configurations with the number of cores is covered by the [ACCESS-NRI Model Scaling Repository](https://github.com/ACCESS-NRI/access-model-scaling/). The studies here usually start from what a scaling notebook found, and look into it in more detail.

## Where do I ask questions?

We welcome feedback and contributions through the [ACCESS-Hive forum](https://forum.access-hive.org.au/). Please create a topic in the #technical category and [follow the guidelines for requesting help from ACCESS-NRI](https://forum.access-hive.org.au/t/access-help-and-support/908) should you need it.

## Running the notebooks

The notebooks need to be run on NCI Gadi, as they run the models to generate the profiling data. If you are working with existing data, you can run them on whichever machine the data lives on.

Create a Python virtual environment with a recent version of Python, and install the dependencies in it:

```bash
module load python3/3.12.1
python -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```

The notebooks can then be started on a login node (e.g. through VSCode) or on NCI ARE. On ARE, set the path to the virtual environment in Advanced Settings -> Python or Conda virtual environment base. A "small" compute size is enough, as the experiments run as their own PBS jobs.
