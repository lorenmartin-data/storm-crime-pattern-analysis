# Miami Property Crime and Florida Storm Activity Analysis

## Project Overview

This project explores monthly property crime activity in Miami alongside statewide Florida storm-event frequency during calendar year 2024. The analysis emphasizes the end-to-end analytical process, including data extraction, cleaning, filtering, classification decisions, aggregation, exploratory visualization, statistical analysis, and interpretation.

The goal was to determine whether periods of increased storm activity appeared to coincide with changes in property crime and whether the observed relationship was statistically meaningful.

## Business Question

Do increases in storm-event activity correspond with higher levels of property crime, and could observed patterns help support future law-enforcement planning and resource allocation?

## Tools and Technologies

- MySQL
- Python
- Pandas
- Matplotlib
- SciPy
- Jupyter Notebook
- Pearson Correlation
- Exploratory Data Analysis
- Data Cleaning and Validation

## Analytical Workflow

The project followed an end-to-end analytical process:

1. Extracted crime and storm-event records from MySQL.
2. Reviewed dataset structure, fields, missing values, duplicates, and date ranges.
3. Selected variables relevant to the analytical question.
4. Defined a property-crime subset using applicable incident classifications.
5. Filtered storm-event records to Florida.
6. Converted date fields and aggregated both datasets to the monthly level.
7. Used boxplots and monthly visualizations to examine distributions and possible outliers.
8. Compared monthly property-crime and storm-event patterns visually.
9. Used Pearson correlation to measure the strength and statistical significance of the relationship.
10. Interpreted the findings, limitations, and potential value for future analysis.

## Analytical Decisions

Several judgment calls were required during the analysis.

### Defining Property Crime

The crime dataset did not include a predefined property-crime category. Relevant incident types were therefore selected based on the analytical objective, including categories such as burglary, larceny/theft, stolen vehicles, vandalism, and arson.

### Geographic Scope

Crime records represented Miami, while storm-event frequency was analyzed at the Florida level. The storm dataset did not provide a direct city field that could be simply matched to Miami. Although additional geographic fields were available, more precise matching would require additional geographic or spatial analysis beyond the scope of the original project.

Statewide storm-event frequency was therefore used as an exploratory measure of broader storm activity.

### Common Time Scale

Both datasets were aggregated to the monthly level so crime and storm activity could be compared using a common unit of analysis.

## Key Findings

- Monthly property crime remained relatively stable throughout 2024 compared with the greater variability observed in monthly storm-event frequency.
- Some months with elevated storm activity also showed elevated property crime, but the pattern was not consistent throughout the year.
- Pearson correlation produced a moderate positive relationship of approximately **r = 0.47**.
- The associated **p-value was approximately 0.12**, which exceeded the 0.05 significance level.
- The analysis therefore did not provide sufficient statistical evidence to conclude that monthly storm-event frequency was significantly associated with increased property crime.

## Interpretation

The results illustrate an important distinction between an apparent visual pattern and statistically supported evidence. Although the monthly data showed a moderate positive correlation, the relationship was not statistically significant.

Storm activity alone should therefore not be treated as a reliable explanation for changes in property crime based on the available 2024 data. Additional years of observations and more geographically precise storm information would be needed before stronger conclusions could be drawn.

## Limitations

- Only one calendar year of data was available.
- Miami crime activity was compared with statewide Florida storm-event frequency.
- Property-crime classification required analyst judgment because no predefined property-crime field was available.
- Correlation identifies association rather than causation.
- Additional geographic and multi-year analysis could provide a stronger basis for evaluating long-term patterns.

## Future Analysis

Future work could:

- incorporate multiple years of crime and storm-event data;
- isolate hurricanes, tropical storms, and other severe-weather categories;
- incorporate geographic or GIS-based matching between storm events and crime locations;
- examine crime patterns before, during, and after major storm events;
- develop predictive models using storm severity, seasonality, geography, and historical crime patterns.

## Project Files

- [Python Analysis Notebook](notebooks/)
- [Project Visualizations](images/)
- [Analytical Report](report/)
- [Data Availability](data/)

## Data Note

The original crime and storm-event datasets were provided through university coursework and are not redistributed because no explicit redistribution license was provided.

This repository is presented as a portfolio case study and includes the analytical workflow, code, visualizations, summarized results, and interpretation developed from the analysis.

## Project Background

This analysis was originally developed as part of an applied data analytics course and has been reformatted and expanded as a professional portfolio case study.
