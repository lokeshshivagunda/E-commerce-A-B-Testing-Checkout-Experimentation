E-Commerce Checkout A/B Testing & Experimentation
------------------------------------------------------------------------------------------------------------------------------
An end-to-end A/B testing project designed to evaluate whether a redesigned e-commerce checkout experience improves purchase conversion while maintaining healthy payment, refund, and checkout performance.
--------------------------------------------------------------------------------------------------------------------------------
Project Objective :

The objective was to compare the existing checkout experience (Control) with a redesigned checkout experience (Treatment) and determine whether the change produced a meaningful improvement in customer conversion.
The analysis focused on users who reached the checkout stage rather than all website visitors.


Core Stack : 
Python 3.11+ - Main development language
MY SQL workbench - Data storage and aggregation
Power BI - Reporting and visualization


Python Libraries:
pandas - Data manipulation and analysis
numpy - Numerical computations
scipy - Statistical tests (z-test, chi-square, Mann-Whitney)
sqlalchemy - Database connectivity and ORM
matplotlib - Data visualization
pyodbc - SQL Server driver (ODBC Driver 17 for SQL Server)

Workflow:


A/B testing end to end Project 
End-to-end A/B testing project analyzing whether a redesigned e-commerce checkout experience improved customer conversion and revenue performance.

The project uses MySQL for data preparation and analysis, Python for statistical testing, and Power BI for business reporting and visualization.

Key areas covered:

Analyzed Control (A) vs Treatment (B) groups using SQL.

Measured Conversion Rate, Revenue per Engaged User (RPEU), and daily performance trends.

Used Two-Proportion Z-Test to evaluate conversion-rate significance.

Used Mann–Whitney U Test to evaluate RPEU differences.

Evaluated Payment Failure Rate, Checkout Abandonment Rate, and Refund Rate as guardrail metrics.

Compared the observed conversion lift against a predefined 5% Minimum Detectable Effect (MDE).

Built an interactive Power BI dashboard to communicate experiment results and business impact.

Recommended continued validation because the observed 4.49% relative conversion lift was below the 5% practical significance threshold, despite statistical significance.

# E-Commerce A/B Testing Project Architecture


                         BUSINESS PROBLEM
                                │
                                ↓
                       EXPERIMENT DESIGN
                                │
                     ┌──────────┴──────────┐
                     ↓                     ↓
                  CONTROL              TREATMENT
                     A                     B
                     │                     │
                     └──────────┬──────────┘
                                ↓
                           RAW DATA
                                │
                                ↓
                    DATA EXTRACTION & PREP
                         SQL / BigQuery
                                │
                                ↓
                     EXPERIMENT VALIDATION
                     ┌──────────┴──────────┐
                     ↓                     ↓
                    SRM                   A/A
             Randomization Check    Experiment Setup
                     │                     │
                     └──────────┬──────────┘
                                ↓
                         METRIC ANALYSIS
                                │
              ┌─────────────────┼─────────────────┐
              ↓                 ↓                 ↓
         PRIMARY METRIC    SECONDARY METRICS    GUARDRAILS
              │                 │                 │
        Conversion Rate       Revenue / RPEU    Payment Failure
              │                 │                Abandonment
           Z-Test             Mann-Whitney       Refund Rate
              │                 │
          95% CI             95% CI
              │                 │
              └─────────────────┼─────────────────┘
                                ↓
                    MULTIPLE-METRIC ANALYSIS
                                │
                    ┌───────────┴───────────┐
                    ↓                       ↓
              Bonferroni / BH        False Positive
              Correction              Control
                                │
                                ↓
                         SEGMENT ANALYSIS
                                │
                                ↓
                           POWER BI
                    Dashboard & Visualization
                                │
                                ↓
                   BUSINESS INTERPRETATION
                                │
                                ↓
                    ROLLOUT RECOMMENDATION


### Analysis Flow

**Business Problem → Experiment Design → Data Preparation → Experiment Validation → Metric Analysis → Multiple-Metric Analysis → Segmentation → Power BI → Business Recommendation**



https://github.com/ermusheva/E-commerce-AB-test?utm_source=chatgpt.com
