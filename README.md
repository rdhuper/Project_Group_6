# Project_Group_6

## Test
### Testing

-----------------------------------------

### Class Objectives

#### Day One: Class Objectives

* Students will be able to articulate the requirements for Project 1.

* Students will be able to create new branches with Git.

* Students will be able to push local branches to GitHub.


#### Day Two: Class Objectives

* Project Work

#### Day Three: Class Objectives

* Project Work

-----------------------------------------

### Week Seven | Activities

#### Day One: Activities

* Listed in Slide Deck

#### Day Two: Activities

* Project Work

#### Day Three: Activities

* [01-Par_Null_Hypothesis](activities/day-3/01-Par_Null_Hypothesis)
* [02-TTest](activities/day-3/02-TTest)
* [03-Stu_Sardines](activities/day-3/03-Stu_Sardines)
* [04-ANOVA](activities/day-3/04-ANOVA)
* [05-Stu_ANOVA](activities/day-3/05-Stu_ANOVA)
* [06-Chi_Square](activities/day-3/06-Chi_Square)
* [07-Stu_Chi_Square](activities/day-3/07-Stu_Chi_Square)
* [01-Par_Null_Hypothesis](activities/day-3/01-Par_Null_Hypothesis)
* [01-Par_Null_Hypothesis](activities/day-3/01-Par_Null_Hypothesis)
* [01-Par_Null_Hypothesis](activities/day-3/01-Par_Null_Hypothesis)


-----------------------------------------

### Week Seven | Video Walkthroughs

* None

-----------------------------------------

### Week Seven | Slide Deck

* Day 1: [Slide Deck](resources/day-1)

* Day 2: None

* Day 3: [Slide Deck](resources/day-3)


-----------------------------------------
### Week Seven Homework

* None - Project Work


-----------------------------------------

### Week Seven | Helpful Links

* [Introduction To Git](https://medium.com/@ashk3l/a-visual-introduction-to-git-9fdca5d3b43a)

* [Safest and riskiest areas of New York's subway system revealed in Daily News investigation
](http://www.nydailynews.com/new-york/nyc-crime/daily-news-analysis-reveals-crime-rankings-city-subway-system-article-1.1836918)

* [Bullying Rates Drop](https://www.data.gov/education/bullying-rates-drop)

* [Uber Pickups in New York City](https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city)

### Week Seven | Terminology


# Branch Demo

## 0. Getting the Repo

Before we can work with Git, we must either **create a new repository**, or **clone one from GitHub**.

Note that, in the examples below, we use `git status` before every `git commit`. This is a best practice that helps ensure a deliberate commit history. For brevity's sake, this line will be omitted in future files, **but assume we've always run `git status` before any `git commit`**.

### Clone from GitHub

If someone has already shared a repository on GitHub, you can **clone** it to your local machine with \`git.

```bash
# Clone an existing repo.
git clone <repo_url>
# Navigate into newly created repo directory
cd <repo_name>
```

## 1. Add Files

Next, we simply develop as normal, and `commit` our changes whenever we make significant progress.

In general, it's best to **commit early** and **commit often**. Frequent snapshots ensure you'll never be far away from a "last working version".

```bash
# Create a file, called clean_data.py
touch clean_data.py

# Add and commit clean_data.py...
git add clean_data.py
git status
git commit -m "First commit."

# Add cleanup code to clean_data.py...
git add clean_data.py
git status
git commit -m "Clean up provided data."

# Add code to export clean data...Note that `add .` adds
# everything in the current folder
git add .
git status
git commit -m "Export clean data as CSV."
```

## 2. Create Branches

To create a new, isolated development history, we must create **branches**.

```bash
# Create new branch and switch to it
# Long form: `git checkout --branch data_analytics`
git checkout -b data_analytics
```

Alternatively, we can create a branch and then switch to it as two separate steps, though this is uncommon.

```bash
git branch new_branch_name
git checkout new_branch_name
```

Once we've created a new branch, we can develop as normal:

```bash
# Create file to contain data analysis
git add analysis.ipynb
git status
git commit -m "Add Jupyter Notebook for data analysis."

# Add notebook cells summarizing data
git add analysis.ipynb
git status
git commit -m "Add summary tables to Jupyter Notebook."

# Export analyzed data and/or plots
git add .
git commit -m "Export analysis results and save plots as PNG files."
```

### 3. Merge

Once we've developed and tested the changes on our `data_analysis` branch, we can include them in `master` by **merging** the two branches.

```bash
# Move back to master
git checkout master

# Merge changes on data_analysis with code on master
git merge data_analysis

# Delete the data_analysis branch
git branch -d data_analysis
```

**N.b.**, deleting the `data_analysis` branch isn't necessary, but it's best practice to prune unneeded branches.



------------------------

Projects

# Technical Requirements

The technical requirements for Project 1 are as follows.

* [ ] Use Pandas to clean and format your data set(s)

* [ ] Create a Jupyter Notebook describing the **data exploration and cleanup** process

* [ ] Create a Jupyter Notebook illustrating the **final data analysis**

* [ ] Use Matplotlib to create a total of 6-8 visualizations of your data (ideally, at least 2 per "question" you ask of your data)

* [ ] Save PNG images of your visualizations to distribute to the class and instructional team, and for inclusion in your presentation

* [ ] Optionally, use at least one API, if you can find an API with data pertinent to your primary research questions

* [ ] Create a write-up summarizing your major findings. This should include a heading for each "question" you asked of your data, and under each heading, a short description of what you found and any relevant plots.

------------------------

Presentations

# Presentation Requirements

The presentation requirements for Project 1 are as follows.

Your presentation must:

* [ ] Be at least 8-10 min. long

* [ ] Describe the core message or hypothesis for your project.

* [ ] Describe the questions you and your group found interesting, and what motivated you to answer them

* [ ] Summarize where and how you found the data you used to answer these questions

* [ ] Describe the data exploration and cleanup process (accompanied by your Jupyter Notebook)

* [ ] Describe the analysis process (accompanied by your Jupyter Notebook)

* [ ] Summarize your conclusions. This should include a numerical summary (i.e., what data did your analysis yield), as well as visualizations of that summary (plots of the final analysis data)

* [ ] Discuss the implications of your findings. This is where you get to have an open-ended discussion about what your findings "mean".

* [ ] Tell a good story! Storytelling through data analysis is no different than in literature. Find your narrative and use your analysis and visualization skills to highlight conflict and resolution in your data.

----------------------

# Pull Request Workflow

When working with **Pull Requests**, consider the following workflow.

## Review & Merge

* First, create a repository, and add any collaborators via the settings panel.

* On your local machines, create and work on local branches.

* When you're satisfied with the changes you've made to your local branch and want to merge it into `master`, **push the branch to GitHub**.

  * i.e., run: `git push origin <branch_name>`

* Navigate to your GitHub repository in the browser, and select your branch from the drop-down on the home page.

![GitHub's select for which branch to display.](../Images/branch-select.png)

* Open a pull request against your branch.

![The Create Pull Request button.](../Images/create-pr.png)

* Fill out the form that pops up, and press **Create Pull Request**.

* Be sure to discuss **who is responsible for reviewing PRs, and when**.

-----------------------

* [Hypothesis Testing](http://www.statisticshowto.com/probability-and-statistics/hypothesis-testing/#Hypothesis)

* [The null and alternative hypothesis](https://statistics.laerd.com/statistical-guides/hypothesis-testing-3.php)

* [ T Test ](http://www.statisticshowto.com/probability-and-statistics/t-test/)

* [Chi Square](http://www.statisticshowto.com/chi-square-test-normality/)

* [Chi Square Test](http://www.statisticshowto.com/probability-and-statistics/chi-square/#chisquareqtest)

* [ANOVA](http://www.statisticshowto.com/probability-and-statistics/hypothesis-testing/anova/)


* [Critical Values of the Chi-Square
Distribution](http://www3.med.unipmn.it/~magnani/pdf/Tavole_chi-quadrato.pdf)

* [Confidence Interval](http://www.statisticshowto.com/probability-and-statistics/confidence-interval/)

* [stats.ttest_ind](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html)

* [ttest_1samp](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_1samp.html)

* [](https://docs.scipy.org/doc/scipy-0.18.1/reference/generated/scipy.stats.f_oneway.html)
