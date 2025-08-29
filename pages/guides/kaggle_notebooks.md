# Using Kaggle notebooks

Kaggle offers free compute (including 30 hour of GPU time per week) via their notebooks feature. See the documentation [here](https://www.kaggle.com/docs/notebooks) for the full details. Kaggle notebooks are a great solution especially, if you are working with a Kaggle dataset or a model that requires GPU compute. There are some advantages and disadvantages to Kaggle notebooks over GitHub Codespaces:

**Advantages relative to GitHub Codespaces:**
1. Much more powerful than a dual core GitHub codespace
2. Integrated directly with Kaggle datasets

**Disadvantages relative to GitHub Codespace:**
1. Limited/no real access to underlying Linux instance
2. Less flexible/more cumbersome, especially for projects with multiple files
3. Risk of causing merge conflicts if you try to use Kaggle and GitHub codespaces on the same project

To illustrate the use of Kaggle notebooks for data science projects, let's walk through setting up the Cats vs Dogs image classifier. These instructions assume you already have a phone number verified Kaggle account, and a project repository that you are working on. If not, fork my [gperdrizet-image-classification repo.](https://github.com/4GeeksAcademy/gperdrizet-image-classification).

**To get started you will need to do ~3 things:**

1. Create a new Kaggle utility script notebook for the helper functions module and import it from GitHub
2. Create a new Kaggle notebook for the image classifier project and import your notebook from GitHub
3. Add the dogs vs cats competition datasource to your Kaggle notebook
4. Add the utility script notebook to the project notebook

Alternatively, you can just work in Kaggle from the get-go - but then you won't be able to run the MVP or any of the solution notebooks.

## 1. Create a Kaggle utility script notebook

This notebook will hold our helper functions module allowing us to import it into our project notebook, just like we would in a Codespace. If the project you are working on is just a single notebook and you are not importing custom functions from another file, you can skip this step.

1. Click your profile icon and select 'Your Work'
2. Click the '+ Create' button and choose 'New Notebook'
3. Name the notebook something descriptive (I chose image_classification_functions to match the module name)
4. Under 'File' click Link to GitHub. (If this is the first time you have linked a notebook, follow the prompts to login and authorize)
5. Under 'File' click 'Import Notebook', select 'GitHub' and paste the full URL to the file on GitHub (not the repo main page!). Mine is [this](https://github.com/4GeeksAcademy/gperdrizet-image-classification/blob/main/notebooks/image_classification_functions.py)
6. Click 'Import'
7. Under 'File', click 'Set as Utility Script'
8. Click 'Save Version', select 'Quick Save' and click 'Continue', then click 'Continue without GitHub'

If you refresh the 'Your Work' page on Kaggle you should now see the new notebook. Now that you have this utility script set up, you can import in into other notebooks. You can also edit it on Kaggle and push it back to GitHub. Or you can work on it somewhere else, and re-import it from GitHub to use the changes on Kaggle.

## 2. Create a Kaggle notebook for the project

1. Click your profile icon and select 'Your Work'
2. Click the '+ Create' button and choose 'New Notebook'
3. Name the notebook something descriptive (I chose tensorflow_cnn_classifier)
4. Under 'File' click Link to GitHub.
5. Under 'File' click 'Import Notebook', select 'GitHub' and paste the full URL to the notebook on GitHub (not the repo main page!). Mine is [this](https://github.com/4GeeksAcademy/gperdrizet-image-classification/blob/main/notebooks/tensorflow_cnn_classifier.ipynb)
6. Click 'Import'

## 3. Add the Dogs vs Cats dataset

1. On the right side under 'Notebook', go to 'Input' and choose '+ Add Input'
2. Select 'Competitions' and search for Dogs vs Cats (you might have to scroll down to find it)
3. Click the plus sign at the bottom right of the competition dataset listing

## 4. Add the helper functions

1. On the right side under 'Notebook', go to 'Input' and choose '+ Add Input'
2. Select the 'Your Work' and 'Utility Scripts' filters and you should see it
3. Click the plus sign

Done! Now you can work in the notebook, just like you would in a Jupyter server running in VSCode on a Codespace or anywhere else. To add a GPU go to 'Settings' -> 'Accelerator'. But be careful, GPUs don't speed all computations up and you only get 30 hours per week for free. Don't waste it!


