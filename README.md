# ds-12
Course materials for ds-12

## Quick reference for commands and libraries

1. [Pandas](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
2. [Git](https://education.github.com/git-cheat-sheet-education.pdf)
3. [Bash commands (linux command line)](https://icosbigdatacamp.github.io/2018-summer-camp/slides/BASH_Cheat_Sheet.pdf)
4. [VScode (windows/linux)](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
5. [VScode (macOS)](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
6. [Jupyter notebooks](https://www.edureka.co/blog/wp-content/uploads/2018/10/Jupyter_Notebook_CheatSheet_Edureka.pdf)


## 2025-06-27

Useful Pandas methods for the real estate data cleanup assignment:

1. `.sort_values()` used to sort a dataframe
2. `.unique()` & `.nunique()` used to get information about unique values in a dataframe/series
3. `.isna()` checks for NaN (not a number) missing value placeholders
3. `.dropna()` used to remove NaN (not a number) missing value placeholder from a dataframe or series

You can find more information about what these methods do and how to use them in the Pandas [DataFrame](https://pandas.pydata.org/docs/reference/frame.html) and [general function](https://pandas.pydata.org/docs/reference/general_functions.html) documentaion.

There is a whole module about plotting comming up - but for now, a quick skim of the Matplotlib [hist](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html) documentation should be enough to complete the last question.

## 2025-07-02

Cool talk by Bohan Zhang of OpenAI's infrastructure team - covers their implementaion of PostgreSQL and shows what is possible with a cutting edge, production grade SQL database at a top company: [OpenAI: Scaling PostgreSQL to the Next Level](https://www.pixelstech.net/article/1747708863-openai%3a-scaling-postgresql-to-the-next-level).