# Retail Analytics Capstone: Marketing Campaign Analytics

## 1. Project Overview

This project explores customer behaviour and marketing campaign
performance using retail customer data. The aim is to support
data-driven marketing decisions by analysing customer demographics,
purchasing patterns, shopping-channel preferences, promotional
engagement, and campaign responses.

The project package includes a customer marketing dataset, a Power BI
report, and supporting project documentation. The analysis can help a
retail business understand which customer groups engage with campaigns,
how customers shop across channels, and which factors may be useful when
planning future marketing activity.

> **Project note:** Validate all findings, KPIs, and conclusions against
> the Power BI report and analysis before presenting them as confirmed
> results.

## 2. Business Problem

Retail marketing teams need to understand their customers and evaluate
campaign engagement so they can make better-informed decisions about
targeting, channel strategy, and promotional activity.

This project uses customer-level data to explore questions such as:

-   Which customer characteristics are associated with different
    purchasing patterns?
-   How do customers use web, catalogue, and in-store purchasing
    channels?
-   How do customers respond to marketing campaigns?
-   What is the relationship between deal purchases, spending, and
    campaign response?
-   Which customer segments could be investigated further for more
    relevant marketing?

These are analytical questions to investigate, not conclusions assumed
in advance.

## 3. Project Objectives

-   Explore customer demographics and household characteristics.
-   Analyse spending across product categories, including wine, fruit,
    meat, fish, sweets, and gold products.
-   Compare purchasing behaviour across web, catalogue, and store
    channels.
-   Examine campaign acceptance and response indicators.
-   Assess customer recency, deal purchasing, and website visit
    patterns.
-   Prepare data for reporting and visualisation.
-   Communicate findings that can inform customer segmentation and
    future campaign planning.

## 4. Dataset

The project includes `marketing_campaign.csv` and
`marketing_campaign.xlsx`.

The CSV dataset contains **2,240 records and 30 columns**. Fields
include:

  ---------------------------------------------------------------------------------
  Data area               Example fields                    Purpose
  ----------------------- --------------------------------- -----------------------
  Customer profile        `ID`, `Year_Birth`, `Age`,        Explore customer
                          `Education`, `Marital_Status`,    characteristics
                          `Income`                          

  Household               `Kidhome`, `Teenhome`             Examine household
                                                            composition

  Customer relationship   `Dt_Customer`, `Recency`,         Explore enrolment date,
                          `Complain`                        recent purchase timing,
                                                            and complaints

  Product spending        `MntWines`, `MntFruits`,          Compare spending by
                          `MntMeatProducts`,                product category
                          `MntFishProducts`,                
                          `MntSweetProducts`,               
                          `MntGoldProds`                    

  Purchase behaviour      `NumDealsPurchases`,              Compare purchase
                          `NumWebPurchases`,                frequency and channels
                          `NumCatalogPurchases`,            
                          `NumStorePurchases`               

  Digital engagement      `NumWebVisitsMonth`               Explore monthly website
                                                            visits

  Campaign outcomes       `AcceptedCmp1`--`AcceptedCmp5`,   Analyse campaign
                          `Response`                        acceptance and response

  Dataset constants       `Z_CostContact`, `Z_Revenue`      Review the meaning and
                                                            use of supplied
                                                            cost/revenue fields
                                                            before analysis
  ---------------------------------------------------------------------------------

### Data preparation considerations

Before drawing conclusions, check:

-   Missing values, especially in `Income`.
-   Duplicate records and the uniqueness of `ID`.
-   Data types and date parsing for `Dt_Customer`.
-   The consistency of age and birth-year fields.
-   The meaning and valid values of campaign indicators.
-   Outliers and implausible demographic or spending values.
-   Whether the dataset's date range and fields are suitable for the
    questions being asked.

Document any exclusions, assumptions, transformations, and calculated
measures so that the analysis is reproducible.

## 5. Technologies and Tools

-   **Microsoft Power BI Desktop** --- report development and data
    visualisation; a `.pbix` report is included in the project files.
-   **Microsoft Excel** --- inspecting and reviewing the tabular
    dataset.
-   **CSV** --- portable source data for analysis.
-   **SQL** --- intended for querying and analysing structured data;
    supporting SQL documentation is included in the project package.
    Confirm the available query content before describing specific SQL
    transformations as completed.
-   **Business Requirements Document (BRD)** --- project planning and
    documentation of objectives, scope, requirements, stakeholders,
    constraints, and cost-benefit considerations.

## 6. Key Analysis Areas

The dataset supports investigation of the following areas:

### Customer segmentation

Explore customer profiles using available demographic, income, and
household fields. Define segment rules clearly and avoid drawing
conclusions from very small groups.

### Product-category spending

Compare spending across product categories and investigate which
customer characteristics correspond with different spending patterns.

### Sales-channel behaviour

Compare web, catalogue, and in-store purchase counts. Investigate how
channel use varies between customer groups.

### Campaign engagement

Compare the supplied campaign acceptance indicators and `Response`.
Confirm the dataset's definitions before interpreting these fields, and
distinguish historical response from predictions about future behaviour.

### Promotions and digital engagement

Explore relationships between deal purchases, website visits, purchase
channels, and campaign responses. Treat observed relationships as
associations unless a suitable method supports causal conclusions.

## 7. Key Features and Deliverables

-   Customer marketing dataset supplied in CSV and Excel formats.
-   Power BI report file for interactive reporting and visual
    exploration.
-   BRD template for documenting the business context and project
    requirements.
-   SQL-related supporting document.
-   An analysis framework covering customer profile, product spending,
    purchase channels, and campaign engagement.

The exact visuals, measures, transformations, and final findings should
be described only after checking the Power BI report and confirming what
has been implemented.

## 8. My Role and Contributions

Use the following as a portfolio-ready outline and edit it to reflect
the work you personally completed:

-   Structured the analysis around a retail marketing problem and
    defined questions to investigate.
-   Reviewed the customer dataset and identified relevant demographic,
    spending, purchasing-channel, and campaign-response fields.
-   Used Excel and/or SQL to inspect, prepare, and analyse data, where
    applicable.
-   Developed or worked on a Power BI report to present customer and
    campaign analysis.
-   Considered data quality checks and the documentation needed to make
    the analysis understandable and reproducible.
-   Interpreted results and considered how findings could support
    customer segmentation and marketing decisions.

**Before publishing:** Keep only the contributions you personally
performed. Add specific measures, DAX calculations, SQL queries, Power
Query transformations, visuals, and quantified findings only if they are
present in your work and can be demonstrated.

## 9. How to Run or Use the Project

### Option A: Open the Power BI report

1.  Download or clone this project repository.
2.  Install Microsoft Power BI Desktop.
3.  Open `Retail Analytics Project.pbix`.
4.  If Power BI requests access to a source file, point it to the
    included dataset or update the data-source path as appropriate.
5.  Refresh the data if required.
6.  Review the report pages, filters, measures, and visuals.
7.  Validate key figures against the source data before using them in a
    presentation.

### Option B: Inspect the dataset in Excel

1.  Open `marketing_campaign.xlsx` in Microsoft Excel, or import
    `marketing_campaign.csv`.
2.  Check column names, data types, missing values, duplicate IDs, and
    unusual values.
3.  Use PivotTables, formulas, or other suitable analysis tools to
    explore customer spending and purchase behaviour.

### Option C: Use SQL

1.  Load the CSV data into a database or SQL environment that supports
    CSV imports.
2.  Define suitable data types and confirm date parsing.
3.  Run SQL queries to profile the data and investigate the analysis
    questions.
4.  Validate query results against Excel or Power BI totals.
5.  Document queries and assumptions used.

The package's SQL document should be checked to confirm which queries or
instructions it contains; database setup details may need to be added
for a fully reproducible SQL workflow.

## 10. Suggested Future Improvements

-   Create a documented data-cleaning and validation workflow.
-   Define a consistent set of business KPIs, including their
    calculation logic.
-   Add clearly labelled report pages for customer profiles, product
    spending, sales channels, and campaign response.
-   Add slicers for relevant customer segments where useful.
-   Include data definitions and a data dictionary.
-   Add a methodology section explaining transformations, assumptions,
    and limitations.
-   If the dataset and business context support it, test a
    campaign-response model using appropriate validation and clearly
    explain its limitations.

## 11. Limitations

-   The dataset is observational; relationships between fields do not
    automatically demonstrate cause and effect.
-   Campaign-response fields need to be interpreted using their
    documented definitions.
-   Missing values, outliers, and data-quality issues may affect
    results.
-   The project files alone do not establish that a specific business
    outcome or uplift was achieved.
-   Any recommendations should be based on verified analysis and should
    consider the dataset's coverage and limitations.

## 12. Repository Structure

``` text
Retail Analytics Capstone/
├── BRD - Retail Analytics Project.pdf
├── marketing_campaign.csv
├── marketing_campaign.xlsx
├── Retail Analytics Project.pbix
└── Retail Analytics SQL.docx
```

## 13. Conclusion

This project provides a foundation for analysing retail customer
behaviour and marketing campaign engagement. By combining customer
profile, product spending, purchase-channel, and campaign-response data,
the analysis can help identify patterns worth investigating and support
more evidence-based marketing decisions. The strength of the final
conclusions depends on careful data validation, transparent methodology,
and verification of the results presented in the Power BI report.
