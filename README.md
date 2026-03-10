# Reporting Automation Tool

Desktop application for automating internal reporting workflows using **Python**, **Flet**, **Pandas**, and **OpenPyXL**.

> Note: the production source code is private because the project was developed for internal commercial use.  
> This repository is a public showcase that describes the problem, architecture, and implementation approach without exposing proprietary code or data.

---

## Overview

This project was built to reduce manual work in recurring internal reporting processes.

The application provides a desktop interface for selecting source files, configuring report parameters, validating input, and generating Excel reports from templates.

The solution focuses on:

- CSV data processing
- Excel report generation
- desktop UI for non-technical users
- validation and error handling
- modular project structure for multiple report types

---

## Problem

Before automation, report preparation required repetitive manual work:

- opening and checking source files
- extracting required values
- transforming data into report-ready format
- filling Excel templates manually
- validating results before delivery

This process was time-consuming, error-prone, and inconvenient for repeated internal use.

---

## Solution

I developed a desktop application that automates the reporting flow:

- reads and processes source CSV data
- applies report-specific calculations and transformations
- fills Excel templates using predefined placeholders and formatting logic
- saves generated reports with structured output naming
- provides a user-friendly desktop UI for configuration and execution
- handles common input issues and invalid file states

---

## My Contribution

I was responsible for:

- application architecture
- UI implementation
- data processing pipeline
- Excel generation logic
- validation and error handling

---

## Tech Stack

- **Python**
- **Flet** — desktop UI
- **Pandas** — tabular data processing
- **OpenPyXL** — Excel generation and template handling

---

## Key Features

- Desktop interface for report generation
- Input file and output directory selection
- Configurable report parameters
- Validation of required inputs before execution
- Excel report generation from templates
- Modular handling of different report types
- Friendly error messages for common user mistakes
- Persistent settings for repeated use
- Smoke-test mode for quick validation without full UI flow

---

## Architecture

The project was structured into separate layers instead of keeping all logic in one script.

### Main logical parts

- **UI layer**  
  Handles user interaction, input forms, file selection, validation messages, and report execution flow.

- **Parsing layer**  
  Reads and prepares source data from CSV files.

- **Calculation layer**  
  Applies report-specific transformations and calculation rules.

- **Excel layer**  
  Generates final `.xlsx` files using templates, formatting, placeholders, and sheet operations.

- **Report registry / configuration layer**  
  Makes it easier to support multiple report types in a scalable way.

### Simplified flow

```text
User input -> validation -> CSV parsing -> data transformation -> Excel generation -> output file
