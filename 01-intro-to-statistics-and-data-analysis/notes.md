# Ch. 1 : Introductions to Statistics and Data Analysis

<script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script>

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
    - Scatter Plot
    - Stem-and-Leaf Plot -> allow to see the distribution of data (alt: _Frequency Distribution_)
    - Histogram -> allow to see the distribution of data
    - Box-and-Whisker Plot or Box Plot -> visibility of median, quartiles, outliers, and tails of distribution
    - Density Plot
    - etc
    - 
