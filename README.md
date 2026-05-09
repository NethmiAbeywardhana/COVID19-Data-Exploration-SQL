# COVID-19 Data Exploration using SQL

## Project Overview

This project explores global COVID-19 data using SQL Server.
The analysis focuses on infection rates, death percentages, vaccination progress, and global trends using SQL queries and data exploration techniques.

---

## Tools Used

* Microsoft Excel
* SQL Server
* SQL Server Management Studio (SSMS)
* GitHub

---

## Dataset

The dataset contains COVID-19 deaths and vaccination data, including:

* Total cases
* New cases
* Total deaths
* Population
* Vaccination data

Tables used:

* `CovidDeaths$`
* `CovidVaccinations$`

---

# SQL Skills Demonstrated

This project demonstrates the use of:

* SELECT Statements
* Filtering Data with WHERE
* Sorting Data with ORDER BY
* Aggregate Functions
* GROUP BY
* JOINS
* Common Table Expressions (CTEs)
* Temporary Tables
* Views
* Window Functions
* Data Type Conversion
* Running Totals

---

# Project Objectives

## 1. Explore COVID-19 Death Data

Analyzed total cases, total deaths, and population data by country and date.

## 2. Calculate Death Percentage

Compared total cases vs total deaths to understand the likelihood of death after contracting COVID-19.

## 3. Analyze Infection Rates

Calculated the percentage of population infected in different countries.

## 4. Identify Countries with Highest Infection Rates

Used aggregate functions and grouping to find countries with the highest infection rates compared to population.

## 5. Identify Countries and Continents with Highest Death Counts

Analyzed total deaths by country and continent.

## 6. Analyze Global Numbers

Calculated global total cases, total deaths, and global death percentage.

## 7. Explore Vaccination Progress

Used window functions to calculate rolling vaccination totals and percentage of population vaccinated.

---

# Key SQL Concepts Used

## Joins

Combined death and vaccination datasets using:

```sql
JOIN Project01..CovidVaccinations$ vac
ON dea.location = vac.location
AND dea.date = vac.date
```

## Window Functions

Used rolling totals to track vaccinations over time:

```sql
SUM(CONVERT(int,vac.new_vaccinations))
OVER (Partition by dea.Location Order by dea.location, dea.Date)
```

## CTE (Common Table Expression)

Used CTEs to simplify complex calculations.

## Temporary Tables

Created temporary tables for reusable analysis.

## Views

Created a SQL view for future visualization and reporting.

---

# Sample Analysis Performed

* Total Cases vs Total Deaths
* Total Cases vs Population
* Countries with Highest Infection Rates
* Countries with Highest Death Counts
* Continent-wise Death Analysis
* Global COVID Statistics
* Rolling Vaccination Analysis

---

# Files Included

* `SQLQuery.sql` → Main SQL project file
* `README.md` → Project documentation

---

# Learning Outcome

Through this project, I improved my understanding of:

* SQL data exploration
* Query optimization
* Window functions
* Analytical thinking using real-world datasets
* Data analysis workflow

---

# Future Improvements

* Build Power BI dashboard using this dataset
* Create visualizations for vaccination trends

---

# Author
Nethmi Abeywardhana


