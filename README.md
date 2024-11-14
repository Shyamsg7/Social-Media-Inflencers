# Identifying Emerging Social Media Influencers in AI

## Description

This project aims to identify influential and emerging social media users within the AI field. The analysis includes data cleaning, preprocessing, and graph-based analysis to uncover relationships between users and key opinion leaders (KOLs). By applying network analysis techniques, we measure user influence and detect potential emerging influencers based on follower relationships, occupations, and centrality metrics.

## Table of Contents

- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features and Methods](#features-and-methods)
- [Key Files](#key-files)

## Usage

1. Open the notebook and execute cells in sequence.
2. Customize file paths and parameters as needed for data file locations and analysis specifics.

## Project Structure

-**Data Folder (data)**: Contains the dataset file, `final_dataset.xlsx`.

-**Notebook (Final_Project_DA.ipynb)**: Main code file for analysis.

## Features and Methods

### Data Preprocessing

-**Data Loading**: Loads the dataset from an Excel file.

-**Data Cleaning**: Removes rows with missing values in key columns, refines columns like `position_categorized` to maintain consistency, and merges certain columns for a more cohesive analysis.

### Graph Construction and Analysis

-**Graph G1**: Directed graph where nodes represent users, and edges represent following relationships. Key metrics:

  -**Indegree Centrality**: Measures popularity based on followers.

  -**Eigenvector Centrality**: Assesses influence beyond direct followers.

-**Graph G5**: Directed graph focusing on connections between KOLs and other users, including:

  -**Influence Score Calculation**: Uses follower count and degree normalized scores, weighted by an alpha parameter.

### Influencer Identification

-**Emerging Influencers**: Identifies users who have a significant number of KOL followers but lower overall followers, signaling potential for growth in influence.

-**Popular Influencers**: Based on centrality measures, identifies top influencers and examines their occupation and location distribution.

### Helper Functions

-**Data Loading**: `load_excel()` to load data from the specified file.

-**Plot Saving**: `save_fig()` to save plots for consistent project organization.

## Key Files

-**Notebook**: `Final_Project_DA.ipynb` – Contains code for data loading, preprocessing, analysis, and visualizations.

-**Data File**: `final_dataset.xlsx` – Dataset of KOLs and followers for analysis.

-**Plot Folder**: `plot_mine1` – Stores plots generated throughout the analysis.
