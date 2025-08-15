# ds-12
Course materials for ds-12

1. [YouTube playlist](https://www.youtube.com/watch?v=607QEWYZQpU&list=PLjMIC_h0rNV0yY-Nb18MCZRy8XC99xgod)
2. [Module slides](https://github.com/gperdrizet/ds-12/blob/main/pages/slides.md)
3. [Project solutions](https://github.com/gperdrizet/ds-12/blob/main/pages/solutions.md)
4. [Data science project MVPs](https://github.com/gperdrizet/ds-12/blob/main/pages/MVPs.md)
5. [Data science project template repo](https://github.com/gperdrizet/4Geeks_datascience_project)
5. [How-to guides](https://github.com/gperdrizet/ds-12/blob/main/pages/guides.md)


## Extras

## 2025-08-15

I added a short write-up explaining the naive Bayes/bag-of-words classifier example from the lectures slides. See here:

[Bag-of-words/naive Bayes](https://github.com/gperdrizet/ds-12/blob/main/pages/guides/bag_of_words_naive_bayes.md)

## 2025-08-13

Here are links to the documentation to the additional implementation of gradient boosting we discussed in class:

1. DLMC's XGBoost
    - GitHub: [dmlc/xgboost](https://github.com/dmlc/xgboost)
    - PyPI: [xgboost](https://pypi.org/project/xgboost/)
    - Official documentation: [XGBoost documentation](https://xgboost.readthedocs.io/en/stable/)

2. Microsoft's LightGBM
    - GitHub: [microsoft/LightGBM](https://github.com/microsoft/LightGBM)
    - PyPI: [lightgbm](https://pypi.org/project/lightgbm/)
    - Official documentation: [LightGBM documentation](https://lightgbm.readthedocs.io/en/stable/)

## 2025-08-11

Cool paper which first described the idea of using an ensemble of decision trees to help mitigate overfitting issues:

Tin Kam Ho (1995) [Random Decision Forests](https://www.mrcc.purdue.edu/files/Legacy-Research/Random_decision_forests.pdf)

### 2025-08-08

Here are the links to the 'longer-limbs' package that uses linear regression as a fall-back for extrapolation beyond the training data range of a tree based regression model:

1. PyPI: [longer-limbs](https://pypi.org/project/longer-limbs)
2. GiHub: [gperdrizet/longer-limbs](https://github.com/gperdrizet/longer-limbs)

Package was built and published as part of a final project from an earlier cohort.

### 2025-08-06

I added the notebooks for the overfitting demonstration and the fraction of explained variance example which were used to generate the plots in the linear regression slides. Take a look:

1. [R-squared as fraction of explained variance](https://github.com/gperdrizet/ds-12/blob/main/assets/notebooks/explained_variance.ipynb)
2. [Overfitting demo](https://github.com/gperdrizet/ds-12/blob/main/assets/notebooks/overfitting.ipynb)

You can also find them linked via the 'How-to guides' page above.

### 2025-07-23

You will need two statistical test for tonight's assignment: the t-test and ANOVA. Both are in the SciPy stats module.

1. [`ttest_ind`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html): t-test for means in two independent samples.
2. [`f_oneway`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.f_oneway.html): ANOVA for equivalence in means of two or more groups. Note: this test only tells you if one or more groups is significantly different than the others - not which group or groups!

### 2025-07-18

OpenAI just released their ChatGPT based agent yesterday - here are the details:

- Press release/FAQ style overview: [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent)
- Full technical details: [ChatGPT Agent System Card](https://cdn.openai.com/pdf/839e66fc-602c-48bf-81d3-b21eacc3459d/chatgpt_agent_system_card.pdf)


### 2025-07-16

While we are on the 'math' portion of the course one good, if a little obscure, Python library to know about is [SymPy](https://www.sympy.org/en/index.html). It does symbolic math in Python - including derivatives. We won't run into it often, but its good to know its out there in case you ever need it. Here's and example from the documentation - calculating the first derivative of a cosine function:

```python
import sympy as sp

x = sp.symbols('x')
derivative = sp.diff(sp.cos(x), x)

print(f'First derivative: str(derivative)')
```
```text
First derivative: -sin(x)
```


### 2025-07-14

As promised here is an 'extra' assignment which will walk you through hard-coding your own optimizer in Python to fit a linear model to toy data. Highly recommend taking a look - the assignment will give you a good 'gut' feeling for what is happening under the hood when we train machine learning models:

[Linear Regression & Optimization Assignment](https://github.com/4GeeksAcademy/gperdrizet-optimization-bonus-assignment)

2024 Nobel prize in physics was awarded for early research which lead to modern neural networks. The prize was shared between two researchers: John Hopfield, who invented the 'Hopfield network' and Geoffrey Hinton, who designed early gradient descent algorithms.

1. [2024 Nobel Prize in Physics](https://www.nobelprize.org/prizes/physics/2024/popular-information/): description of the history and importance of the works
2. [ADAM: A METHOD FOR STOCHASTIC OPTIMIZATION](https://arxiv.org/pdf/1412.6980): Scientific paper describing ADAM, one of the most common/popular optimization algorithms for training neural networks (note the publication year and the first authors affiliations!).


### 2025-07-11

Interesting further topic to read up on while we are learning about APIs: [Model Context Protocol](https://modelcontextprotocol.io/introduction). MCP was originally proposed by Anthropic, but is an open standard that anyone can use. It's basically a type of API designed for LLMs and agents to use. It standardizes communication between the model and data source, allowing a way to easily use and share tools for building agents. See also [A2A](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) (Google) and [ACP](https://www.ibm.com/think/topics/agent-communication-protocol) (IBM) - same idea, but for communication between agents.


### 2025-07-02

Cool talk by Bohan Zhang of OpenAI's infrastructure team - covers their implementation of PostgreSQL and shows what is possible with a cutting edge, production grade SQL database at a top company: [OpenAI: Scaling PostgreSQL to the Next Level](https://www.pixelstech.net/article/1747708863-openai%3a-scaling-postgresql-to-the-next-level).


### 2025-06-27

Useful Pandas methods for the real estate data cleanup assignment:

1. `.sort_values()` used to sort a dataframe
2. `.unique()` & `.nunique()` used to get information about unique values in a dataframe/series
3. `.isna()` checks for NaN (not a number) missing value placeholders
3. `.dropna()` used to remove NaN (not a number) missing value placeholder from a dataframe or series

You can find more information about what these methods do and how to use them in the Pandas [DataFrame](https://pandas.pydata.org/docs/reference/frame.html) and [general function](https://pandas.pydata.org/docs/reference/general_functions.html) documentation.

There is a whole module about plotting coming up - but for now, a quick skim of the Matplotlib [hist](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html) documentation should be enough to complete the last question.
