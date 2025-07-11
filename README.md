# ds-12
Course materials for ds-12

1. [YouTube playlist](https://youtu.be/607QEWYZQpU?si=rBIrfjwxsHJk3xf4)
2. [Module slides](https://github.com/gperdrizet/ds-12/blob/main/slides.md)
3. [Project solutions](https://github.com/gperdrizet/ds-12/blob/main/solutions.md)
4. [How-to guides](https://github.com/gperdrizet/ds-12/blob/main/guides.md)

## Extras

### 2025-06-27

Useful Pandas methods for the real estate data cleanup assignment:

1. `.sort_values()` used to sort a dataframe
2. `.unique()` & `.nunique()` used to get information about unique values in a dataframe/series
3. `.isna()` checks for NaN (not a number) missing value placeholders
3. `.dropna()` used to remove NaN (not a number) missing value placeholder from a dataframe or series

You can find more information about what these methods do and how to use them in the Pandas [DataFrame](https://pandas.pydata.org/docs/reference/frame.html) and [general function](https://pandas.pydata.org/docs/reference/general_functions.html) documentation.

There is a whole module about plotting coming up - but for now, a quick skim of the Matplotlib [hist](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html) documentation should be enough to complete the last question.

### 2025-07-02

Cool talk by Bohan Zhang of OpenAI's infrastructure team - covers their implementation of PostgreSQL and shows what is possible with a cutting edge, production grade SQL database at a top company: [OpenAI: Scaling PostgreSQL to the Next Level](https://www.pixelstech.net/article/1747708863-openai%3a-scaling-postgresql-to-the-next-level).

### 2025-07-11

Interesting further topic to read up on while we are learning about APIs: [Model Context Protocol](https://modelcontextprotocol.io/introduction). MCP was originally proposed by Anthropic, but is an open standard that anyone can use. It's basically a type of API designed for LLMs and agents to use. It standardizes communication between the model and data source, allowing a way to easily use and share tools for building agents. See also [A2A](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) (Google) and [ACP](https://www.ibm.com/think/topics/agent-communication-protocol) (IBM) - same idea, but for communication between agents.