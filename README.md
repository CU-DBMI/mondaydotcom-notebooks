# mondaydotcom-notebooks
Center-specific notebook logic, mostly with MDC data

# Requirements

This uses the poetry tool.

# Install Poetry

    In my environment I run entirely "path-less", with a number of scripts for each version of Python (e.g python39.cmd, python310.cmd). After each of those scripts is run, I install poetry in each, and proceed from there. Your experience may/will vary.

    pip install poetry

# To work in notebooks

    poetry run jupyter notebook

# To run a notebook on the command line

Note, the `_output` folder must already exist.

    # from the source folder
    cd mondaydotcom-notebooks
    
    poetry run papermill --no-report-mode --log-output "Mondaydotcom Set Task Integration Status.ipynb" "_output\Mondaydotcom Set Task Integration Status.ipynb" 

# Secrets and keys

Keys for MDC and SS are kept in files called `.env-<environment>`, where environment is a parameter passed into the notebook. For example, the environment variable file for `dev` is `.env-dev`. These files are located in the same folder as the notebooks.

## Example .env file:

```
MONDAY_KEY=1234124313109482304238409328402384032840238404380482390
SMARTSHEET_KEY=123980123890123980
```
