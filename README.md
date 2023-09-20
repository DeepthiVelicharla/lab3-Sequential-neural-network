# lab3: Sequential Neural Networks

## Get Started

- Log in and open project in your SageMaker account
- Open a Terminal wiht SMSL Launcher
- Find out, understand, and practice to answer the following questions:
  - where are you in the SMSL file system?
    - Answer: `pwd`
  - what do you currently have in your SMSL account?
    - Answer: `ls -al`
  - what `conda` Python environment is activated and what do you know about it?
    - Answer: `conda info`
  - what are the locations of all `conda` environments you currently have in your SMSL account?
    - Answer: `conda env list` or `conda info --envs`
  - how can you deactivate the currently activated environment? 
    - Answer: `conda deactivate`
  - how can you activate an existing environment, for example **studiolab**?
    - Answer: `conda activate studiolab`
  - how can you create a new virtual environment named `my-special-env`? 
    - Answer: `conda create -n my-special-env`
    - From a `.yml` file named `special_requirements.yml` located in the directory in which we give the command: 
    ```
    conda env create -n my-special-env --file='special_requirements.yml'
    ```
  - how can you find out what packages are installed in the activated environment?
    - Answer: `pip list`
- Change directory to the `comp841` directory in your SMSL **home directory**: 
  - `cd ~; cd comp841`
- Deactivate any current `conda` environment: 
  - `conda deactivate`

Ask questions if you need assistance with `bash` and `conda` tools, or you want to learn more about:
- the structure of a file sytem
- how to navigate through a file system
- the concept of **path**
- what a Python virtual environment is. 

## Get `lab3` repository

- Access the GitHub Classroom activation link posted in your course section Discord channel. 
  - It forks the codebase for the lab into a remote repository in the course GitHub org `github.com/2023-fall-comp-741-841` 
- Get the HTTPS URL of your remote repo from GitHub
- In the SMSL **Terminal** window
  - Check that you are in `comp841`
  - Deactivate current environment
  - Clone the remote repo with the `git` command below and name it`lab3`
    - `git clone <URL of remote> lab3`
  - Check that `lab3` is a new directory in `comp841` and switch to it
    - `ls -al; cd lab3`

## Setup virtual environment

`lab3` is the current directory, also known as **working directory**. 
- Examine the content of the working directory: `ls -al` 
- Create a new virtual environment, `seq-nn`, for this lab:
  - `conda create -n seq-nn python=3.11`
- Verify that `seq-nn` is listed among `conda`'s environments craeted in your SMSL account
  - `conda env list`
- Activate `seq-nn`: `conda activate seq-nn`
- Check what **packages** are **installed by default** in `seq-nn`
  - `pip list`
- Install `ipykernel` with `conda install ipykernel`. This lets the virtual environment be used with JupyterLab.
- Install the following packages: `scikit-learn`, `tensorflow`, `keras`, `pandas`
- This can be done with one command: `pip install keras tensorflow scikit-learn pandas`
- Verify the installation: `pip list`

This environment is used with the `sequential-neural-networks.ipynb` notebook in `lab3`.

## Requirements

- Add Markdown cells before every code cell
    - Explain, *in your own words*, what each code cell is doing.
    - Refer to this [GitHub page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for more information on formatting Markdown.
- Graduate students only: Answer the questions at the end of the notebook.
- Use version control to document your development of the Markdown explanations in the `sequential-neural-networks.ipynb` file
  - `git add .` to stage or index the change you've made
  - `git commit -m 'meaningful message'` to commit to the lab commit history the change

## Submission

- Prior to any push, clear the outputs by selecting `Restart Kernel and Clear...` from the Kernel dropdown menu
- Push the local commit history to the remote: `git push origin main` 
