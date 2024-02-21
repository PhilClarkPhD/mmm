# Example Problem: JellyPop

The marketing team at a growing candy manufacturer, JellyPop, is under pressure from executives to demonstrate that their media strategy is working. They hire us to help them quantify the efficiency of their advertising and tune their investments in various paid channels. They have prepared the file 'marketing_data.csv' for us to work with.

During a call, they tell us that they would like to be able to answer the following questions:
1. Which channels are performing well?
2. Which channels are performing poorly?
3. Assuming they have $1M to spend across their paid media in the coming months, what is the optimal mix of spend across each channel?

Finally, the head of marketing is worried that the executive team will be skeptical of fancy modeling techniques. He asks us to help him convince leadership that our MMM model is trustworthy.

# The MMM Approach
Recent changes in [app tracking](https://purevisibility.com/app-tracking-changes/) and [consumer data protections](https://gdpr-info.eu/) have made it harder for marketers to observe consumer behavior at the most granular level. However, these changes have also allowed for a resurgence of marketing mix modeling (MMM). As a top-down modeling approach, MMM allows companies to identify media efficiency using only aggregate data. In addition to estimating the efficiency of current investments, a *good* MMM model offers the ability to precisely tune future investments to get the best possible returns. 

From a modeling standpoint, MMM can be quite tricky. For example, we must account for media-specific effects such as **adstock** and **saturation**. Adstock reflects a time-lag of media spend on our KPI (a TV ad bought today may drive sales over the next few weeks), and saturation reflects the idea of an upper limit on the efficiency of our media investments (if you spend 1 dollar in advertising to sell 1 Kit Kat, you can't expect to spend $1B and sell 1B Kit Kats). Furthermore, a critical detail we gathered from our conversation with the folks at JellyPop is that our model should capture causal relationships in the data. That is, our forecasts need to hold up if and when we change the amount of spend in each channel. In addition, there are seasonal considerations, multicollinearity and upper vs lower funnel effects to contend with. [Recast](https://getrecast.com/blog/) has a number of excellent blog posts on these and other topics.

In the *mmm.ipynb* notebook, I walk through a simple model development process to address the questions and concerns from the good people at JellyPop.

# Files:
* *mmm.ipynb*: The notebook with the MMM code
* *marketing_data.csv*: An example MMM dataset modified from [this](https://www.kaggle.com/datasets/yugagrawal95/sample-media-spends-data) kaggle dataset
