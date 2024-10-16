# Ch. 1 : Introductions to Statistics and Data Analysis

- [Ch. 1 : Introductions to Statistics and Data Analysis](#ch-1--introductions-to-statistics-and-data-analysis)
  - [Statistical Inference, Samples, Populations, and the Role of Probability](#statistical-inference-samples-populations-and-the-role-of-probability)
  - [Collection of Samples](#collection-of-samples)
    - [Role of Probability in Inferential Statistics](#role-of-probability-in-inferential-statistics)
  - [Descriptive Statistics](#descriptive-statistics)
  - [Discrete and Continuous Data](#discrete-and-continuous-data)
  - [Statistical Modeling, Scientific Inspection, and Graphical Diagnostics](#statistical-modeling-scientific-inspection-and-graphical-diagnostics)
  - [General Type of Statistical Studies](#general-type-of-statistical-studies)


## Statistical Inference, Samples, Populations, and the Role of Probability

```mermaid
mindmap
    root("`**Statistical Methods**`")
        ["`**_Inferential Statistics_**`"]
            to gather "Scientific Information"
                systematic study by conducting ...
                        Experimental Design
                        Observational Study
                        Retrospective Study
                ["`in the form of **_Samples_**`"]
                    ("`are part of a **_Population_**`")
            quantify the "confidence" using
                ["`**_Probability_**`"]
        deal mainly with
            ["`**_Uncertainty_**: variation between observed data and tre property`"]
            ["`**_Variability_**: variation between collected data`"]
        ["`**_Descriptive Statistics_**`"]
            to get summary of data
```

## Collection of Samples

```mermaid           
mindmap
    root("`Collection of Samples`")
        Simple Random Sampling
        Biased Sampling
        Stratified Random Sampling: random sampling within each stratum
```

### Role of Probability in Inferential Statistics

```mermaid
flowchart LR;
    A("`Population`")--"Probability" (Deductive Approach)-->B;
    B("`Sample`")--"Statistical Inference" (Inductive Approach)-->A;
```

## Descriptive Statistics

```mermaid
mindmap
    root("`Descriptive Statistics`")
        Measure of Location
            Means: numerical average; "centroid" of data
            Medians: middle value; "true center" of data 
            Others
                Trimmed Means: eliminate n% of the largest and smallest values
        Measure of Variability
            Standard Deviations
            Variance
        ["`Degree of Freedom (_n-1_): number of independent pieces of information available for computing variablity`"]
        ["`Important measurement (Population Parameters)`"]
            Mean
            Variance
```

## Discrete and Continuous Data

```mermaid
mindmap
    root("`Data`")
        Continuous
        Discrete
            Count data
            Binary data
                Sample proportion  = sample mean
```

## Statistical Modeling, Scientific Inspection, and Graphical Diagnostics

- End result of statistical analysis: **estimation of parameters of a postulated model**
- Make a model based on assumptions on population data
    - Distribution of data is normal/Gaussian
    - etc
- Need characterize the nature of a data
    - Insight from graphical diagnostic -> help highlighting violation of assumptions
    - Do _Exploratory Data Analysis_ (EDA)
- Graphical data
    - [Scatter Plot](https://en.wikipedia.org/wiki/Scatter_plot)

    ![scatter-plot-example](https://upload.wikimedia.org/wikipedia/commons/a/af/Scatter_diagram_for_quality_characteristic_XXX.svg)

    - [Stem-and-Leaf Plot](https://en.wikipedia.org/wiki/Stem-and-leaf_display) -> allow to see the distribution of data (alt: _Frequency Distribution_)

    ![stem-and-leaf-plot-example](https://mathspace-production-media.mathspace.co/media/upload/images/001_Chapter_Entries/Data_Analysis/stem-and-leaf-plot.png)

    - [Histogram](https://en.wikipedia.org/wiki/Histogram) -> allow to see the distribution of data

    ![histogram-example](https://upload.wikimedia.org/wikipedia/commons/1/1d/Example_histogram.png)

    - [Box-and-Whisker Plot or Box Plot](https://en.wikipedia.org/wiki/Box_plot) -> visibility of median, quartiles, outliers, and tails of distribution
  
    ![box-plot-example](https://upload.wikimedia.org/wikipedia/commons/f/fa/Michelsonmorley-boxplot.svg)

    - [Density Plot](https://www.geeksforgeeks.org/density-plots-with-pandas-in-python/)

    ![density-plot-example](https://media.geeksforgeeks.org/wp-content/uploads/20201116233017/speeding.png)

    - [Violin Plot](https://en.wikipedia.org/wiki/Violin_plot)

    ![violin-plot-example](https://upload.wikimedia.org/wikipedia/commons/3/3a/Violin_plot.gif)

    - etc

## General Type of Statistical Studies

```mermaid
mindmap
    root("`Statistical Studies`")
        Designed Experiment
        Observational Study
        Restrospective Study
```

- Interaction
  - When studying a simple experiment with two factors, we need to know whether the factors are interacting or not
  - Parallelism happened when the two factors are not interacting, producing parallel line when connecting the sample means