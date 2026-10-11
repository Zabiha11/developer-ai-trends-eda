# Developer AI Trends: Exploratory Data Analysis

### Exploring AI Adoption, Developer Attitudes, Experience, and Career Trends

## 📌 Overview

Artificial Intelligence is changing how software developers write code,
learn new technologies, and approach their work. However, developers
have different levels of AI adoption, trust, and confidence in
AI-powered tools.

**Developer AI Trends EDA** is a data analysis project that explores
developer survey responses to understand how AI adoption relates to
developer roles, professional experience, attitudes toward AI, AI-agent
usage, and job satisfaction.

Using Python, Pandas, Matplotlib, and Seaborn, this project transforms
raw survey data into meaningful visualizations and insights.

## 🎯 Objectives

-   Explore the demographic and professional characteristics of
    developers.
-   Understand AI tool adoption across developer roles.
-   Investigate the relationship between work experience and AI usage
    patterns.
-   Analyze developers' trust in AI-generated output and their
    perceptions of AI capabilities.
-   Explore AI-agent adoption and its perceived impact on development
    work.
-   Examine developer sentiment toward AI.
-   Investigate the association between AI adoption and job
    satisfaction.
-   Explore compensation patterns across AI usage groups.
-   Present findings through clear and informative visualizations.

## 📂 Dataset

The project uses a developer survey dataset obtained from Kaggle.

  Attribute                     Details
  ----------------------------- --------------------------------------
  Dataset file                  `survey_results_public.csv`
  Original dataset size         49,123 rows × 170 columns
  Selected analysis variables   22 columns
  Data type                     Structured survey data
  Domain                        Software development and AI adoption

The analysis focuses on a selected set of variables related to
demographics, education, employment, work experience, developer roles,
AI usage, AI sentiment, AI models, AI agents, and job satisfaction.

**Dataset source:** [Kaggle](https://www.kaggle.com/datasets)

Search for the original dataset title and add its exact Kaggle URL here.

> The dataset contains missing values, including in conditional AI-agent
> and technology-related questions. Missing responses must be
> interpreted in the context of the original survey questions.

## 🛠️ Technologies Used

-   **Python** --- data analysis and scripting
-   **Pandas** --- data manipulation, cleaning, grouping, and
    cross-tabulation
-   **NumPy** --- numerical operations and missing-value handling
-   **Matplotlib** --- charts and data visualization
-   **Seaborn** --- statistical plots
-   **Jupyter Notebook** --- interactive analysis

## 🔍 Project Workflow

### 1. Data Loading and Initial Inspection

-   Loaded the survey data into a Pandas DataFrame.
-   Inspected sample records, dimensions, column names, and data types.
-   Examined descriptive statistics and missing-value counts.
-   Calculated missing-value percentages to understand data quality.

### 2. Column Selection

Selected 22 variables relevant to the project's main questions.

**Demographics and professional background** - `Age` - `EdLevel` -
`Employment` - `Country` - `DevType` - `Industry` - `RemoteWork`

**Experience and satisfaction** - `WorkExp` - `YearsCode` - `JobSat`

**AI adoption and attitudes** - `AISelect` - `AISent` - `AIThreat` -
`AIAcc` - `AIComplex` - `AIFrustration`

**AI models and agents** - `AIModelsHaveWorkedWith` -
`AIModelsWantToWorkWith` - `AIAgents` - `AIAgentChange` -
`AIAgent_Uses` - `AIAgentKnowledge`

### 3. Data Cleaning and Preparation

The notebook explores and prepares the selected data through operations
including:

-   Checking for duplicate records and removing duplicates.
-   Inspecting missing values in individual columns.
-   Converting selected experience and satisfaction variables to numeric
    types.
-   Standardizing selected categorical values for easier interpretation.
-   Inspecting unusual or unexpected values.
-   Handling missing responses in selected categorical variables.
-   Splitting multi-select AI model responses into individual model
    names for frequency analysis.
-   Creating work-experience groups for comparisons.

Missing values are not necessarily errors in survey data. Some questions
apply only to respondents with particular experiences or tool usage, so
missingness should be considered before deciding how to handle it.

### 4. Exploratory Data Analysis

The analysis uses frequency distributions, percentages,
cross-tabulations, grouped comparisons, and visualizations to
investigate patterns in the survey responses.

## 📊 Key Analysis Areas

### 1. Who Are the Developers?

Explores the distribution of developer age groups and professional
backgrounds.

Visualizations include: - Age distribution - Developer work arrangements

### 2. AI Adoption Across Developer Roles

Investigates differences in AI usage patterns among the most common
developer roles.

Visualization: - Stacked bar chart comparing AI adoption across
developer roles

### 3. AI Adoption and Professional Experience

Examines how AI usage varies with years of work experience.

The notebook groups developers into experience ranges and compares the
percentage distribution of AI usage categories.

Visualizations include: - AI adoption across work experience - AI usage
by experience group - AI sentiment across experience groups

### 4. Do Developers Trust AI?

Explores how developers perceive AI-generated output and its ability to
handle complex tasks.

Visualizations include: - Developer trust in AI accuracy - Perceptions
of AI performance on complex tasks

### 5. AI-Agent Adoption

Investigates the reported adoption of AI agents and whether developers
perceive changes in their development work.

Visualizations include: - AI-agent usage distribution - Perceived impact
of AI agents on development work

### 6. AI Adoption and Developer Sentiment

Analyzes how developers feel about AI and compares sentiment across AI
usage frequencies.

Visualizations include: - Overall AI sentiment distribution - Positive,
neutral, negative, and unsure sentiment categories - AI sentiment by
usage frequency

### 7. AI Adoption and Job Satisfaction

Compares average reported job satisfaction across AI usage categories.

This analysis explores whether differences in job satisfaction are
associated with AI adoption. It does not establish that AI usage causes
higher or lower job satisfaction.

### 8. AI Models Used by Developers

Identifies frequently reported AI models by splitting multi-select
responses and counting individual model names.

Visualization: - Top 10 AI models used by developers

### 9. Additional Statistical Visualizations

The notebook also explores:

-   AI adoption by the most common developer roles
-   Perceived AI-related job threat across experience groups
-   Yearly compensation distributions across AI usage categories
-   Work-experience distributions across AI threat categories
-   Correlations among selected numerical variables

Compensation visualizations filter extreme values for readability. Such
filtering changes the displayed distribution and should be considered
when interpreting results.

## 💡 Preliminary Insights

One observation recorded in the analysis is that **daily AI usage is
more prevalent among developers with fewer years of work experience**,
while the proportion reporting that they do not plan to use AI is higher
among developers with 21 or more years of experience.

This is an observed association in the analyzed survey data, not
evidence that work experience itself causes differences in AI adoption.

Additional findings should be documented after validating the relevant
percentages, sample sizes, and visualizations.

## 🚀 How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook.

### 1. Clone the repository

``` bash
git clone https://github.com/YOUR_USERNAME/developer-ai-trends-eda.git
cd developer-ai-trends-eda
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Create a virtual environment (recommended)

``` bash
python -m venv .venv
```

Activate it on Windows:

``` bash
.venv\Scripts\activate
```

### 3. Install dependencies

``` bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Place the dataset

Download the original survey CSV from its Kaggle source and place it
where the notebook expects to find it:

``` text
survey_results_public.csv
```

The notebook currently loads the file using:

``` python
df = pd.read_csv("survey_results_public.csv")
```

If you store the dataset in a separate directory, update the file path
accordingly.

### 5. Run the notebook

``` bash
jupyter notebook
```

Open `Zabi_EDA_Project.ipynb` and execute the cells in order.

## 📁 Repository Structure

``` text
developer-ai-trends-eda/
│
├── Zabi_EDA_Project.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    └── README.md
```

The raw dataset can be downloaded separately rather than committed to
the repository. The `data/README.md` file can contain the original
dataset URL and instructions for obtaining it.

## ⚠️ Limitations

-   Survey responses represent the participating respondents and may not
    represent all software developers.
-   Missing values and conditional questions can affect comparisons.
-   Self-reported AI usage, sentiment, compensation, and experience may
    contain reporting inconsistencies.
-   Group-level differences do not establish causation.
-   Extreme compensation values can affect statistical summaries and
    visualizations.
-   Results depend on the dataset version, survey year, and question
    wording.

## 🔮 Future Improvements

-   Add a concise executive summary with validated numerical findings.
-   Improve missing-value handling and document the rationale for each
    imputation.
-   Add statistical tests to evaluate selected group differences.
-   Analyze open-ended survey responses using NLP.
-   Develop an interactive dashboard to explore AI adoption by role and
    experience.
-   Improve chart annotations and include sample sizes alongside
    percentages.

## 👩‍💻 Author

**Zabiha Muskan K**

Computer Science Engineering \| Python \| Data Analysis \| AI/ML

GitHub: [@Zabiha11](https://github.com/Zabiha11)

------------------------------------------------------------------------

*This project demonstrates practical skills in data inspection, data
cleaning, exploratory analysis, statistical comparisons, and data
visualization using Python.*
