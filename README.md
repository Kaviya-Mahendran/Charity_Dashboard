# Charity Shop Performance Dashboard

**A. Project Overview**
This repository contains a complete Power BI driven dashboard analytics solution for charity data. The goal is to move beyond static reports and spreadsheets toward an interactive, repeatable, and decision focused dashboard that helps stakeholders understand key patterns in donor behaviour, sentiment, and organisational characteristics.
Unlike dashboards that are built to “look nice,” this one is designed to highlight:
What drives donor engagement?
How do sentiments vary across categories?
Which charity segments show different trends?
Where intervention or focus can improve impact?
This project integrates structured data from ELT/ETL pipelines, NLP outputs, and performance optimized measures to create a dashboard that supports evidence based decision making.
Although implementations vary across organisations, these principles apply broadly to most data analytics environments.

**B. System Architecture Diagram**
Here’s how the dashboard fits into a larger analytics pipeline:

Data Sources
   ↓
ETL / ELT Pipeline
  (cleaning & shaping)
   ↓
Analytics Dataset
   ↓
Power BI Data Model
   ↓
Interactive Dashboard
   ↓
Stakeholder Insights
This architecture ensures that the dashboard sits on clean, governed, and reusable data structures, not raw or one off extracts.

**C. Step by Step Workflow Explanation**
**Step 1: Prepare the Data Model**
The dashboard’s backbone is a clean analytical data model. Before loading into Power BI:
All datasets are transformed into tidy tables
Keys and relationships are clearly defined
Grain of each fact table is explicit
This stage ensures filters, slicers, and visuals behave predictably.

**Step 2: Import into Power BI
Within the .pbix file:**
Tables are loaded using Power Query
Data types are enforced
Relationships are set to many to one, avoiding unnecessary cross filters
This makes the model reliable and scalable.

**Step 3: Define Measures Using DAX**
Key performance indicators (KPIs) are defined using DAX measures rather than calculated columns. This ensures:
performance is optimised
context changes safely with slicers
calculations are consistent across visuals
Example measure:

Total Donors :=
DISTINCTCOUNT ( dim_donor[donor_id] )
This measure becomes reusable throughout the dashboard.

**Step 4: Build Visuals Aligned to Questions**
Visuals are designed with specific analytical questions in mind:
Time trends for donation patterns
Cohort retention charts
Sentiment distributions by category
Segment performance comparisons
Each visual is built to support a decision, not just display a number.

**Step 5: Validate Interactivity and Logic**
Before publishing:
Filters are tested
Totals are validated against source data
Edge cases (nulls, missing data) are handled
This validation ensures the dashboard doesn’t break under real user interaction.

**D. Why This Matters**
Reduces manual reporting
Instead of pulling spreadsheets and manually updating charts, stakeholders have a dynamic interface with built in filters and logic.
Supports evidence based decisions
This dashboard shows not just outcomes (like totals) but drivers (patterns over time, behaviour by segment, sentiment variation). It allows teams to ask why as well as what.
Enables scaled insights
With consistent measures, interactive exploration, and governed data, this dashboard becomes part of the organisation’s analytical infrastructure usable across teams and over time.
Although implementations vary across organisations, these principles apply broadly to most data analytics environments.

**E. Reflection & Learnings**
Building this dashboard reinforced that useful dashboards are not about visuals; they are about questions.
Some core learnings from this process:
Measure definitions must be centralised. When KPIs are defined once in DAX, not repeatedly in visuals, truth becomes consistent.
Data models should force discipline, not flexibility. A right sized model makes analytics safer and faster.
Testing interactivity matters as much as building visuals. A well designed filter should not break the logic of a chart.
From a leadership perspective, this project illustrates a transition from reporting to analytical product thinking. The dashboard is not a static artefact; it is a living interface between data and decisions.
For analysts, the key takeaway is to design dashboards for questions, not charts and to build the underlying models before building the visuals.

**How to Use This Repository**
Clone the repository

git clone https://github.com/Kaviya Mahendran/Charity_Dashboard
Open the .pbix file in Power BI Desktop
Ensure that data sources are accessible and paths are correctly configured
Refresh the data
Explore the interactive reports and filters

**Final Note**
This dashboard is not just a visualisation; it’s a decision support system grounded in clean data, strong modelling, and thoughtful design. It reflects a shift toward analytics that can be extended, maintained, and owned over time not just delivered once.


