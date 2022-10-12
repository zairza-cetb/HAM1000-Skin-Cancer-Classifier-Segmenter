# Contribute

Contributions of any kind (pull requests, bug reports, feature requests, documentation, design) are more than welcome!

## How to Contribute

### Fork the repository

To contribute to HAM10000, you must fork the [HAM10000 Repository](https://github.com/zairza-cetb/HAM10000)

### Setup Environment

1. We are using python notebooks for development here. And it's suggested to go for [Colab](https://colab.research.google.com) instead of Jupyter Notebook. Use the 'setting up environment' part of [reference notebook](https://github.com/zairza-cetb/HAM10000/blob/main/IPYNBs/ashindustry007.ipynb) for setting up the environment.

2. To make a connection of colab and kaggle you must open a [kaggle](https://www.kaggle.com/) account.

3. Then go to your kaggle [account](https://www.kaggle.com/account) and scrool down to find API section where you can click 'Create New API Token' button to download the 'kaggle.json' file.

<p align="center">
  <img alt="logo" src="./src/images/Screenshot 2022-10-12 143741.png">
</p>

  Upload the 'Kaggle.json' file in your colab environment and run the codes below.

  The code below will link the kaggle API with your colab environment. Using Kaggle's beta API, you can interact with Competitions and Datasets to download data, make submissions, and more via the command line.

```bash
! pip install -q kaggle
! mkdir ~/.kaggle
! cp kaggle.json ~/.kaggle/
! chmod 600 ~/.kaggle/kaggle.json
```
  The code below would download the dataset in a compressed format and then extract it in the environment making it available in the scope of program to use it.

```bash
! kaggle datasets download -d surajghuwalewala/ham1000-segmentation-and-classification
! unzip /content/ham1000-segmentation-and-classification.zip
```
### Resolving Issues

You must complete the task or resolve the bugs and keep the output intact while saving the files. Download the file in IPYNB format and rename it as 'your github.ipynb' i.e., ashindustry007.ipynb. You must add the file in the [IPYNBs](https://github.com/zairza-cetb/HAM10000/tree/main/IPYNBs) folder through a PR/MR.

### Create a pull request

After making your changes, open a pull request (PR). Once you submit your pull request, I will review it.
Did you have an issue, like a merge conflict, or don't know how to open a pull request? Check out [GitHub's pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests) tutorial on how to resolve merge conflicts and other issues.
