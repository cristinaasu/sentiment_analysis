# Sentiment Analysis of Financial News

This repository contains the complete codebase, dataset, and paper for a quantitative study of how financial news sentiment affects daily stock price changes and return direction for three major technology firms: Netflix, Amazon, and Meta.

## Overview

This project explores whether the tone of daily headlines from the New York Times can explain short-run stock market movements. Combining text analysis with causal econometric modeling, we assess whether firm-specific sentiment influences next-day returns after accounting for macroeconomic conditions and market-wide factors.

We focus on Netflix, Amazon, and Meta because they:
- Have clear ticker-name mappings for text matching.
- Are frequently covered by financial media.
- Represent a range of business models and investor profiles.

## Methodology

We apply a layered regression strategy:
- Baseline OLS to estimate unconditional sentiment–return relationships.
- Extended OLS models with macroeconomic and financial controls.
- Fixed Effects (FE) to absorb unobserved time variation.
- Instrumental Variables (IV/2SLS) using lagged sentiment to reduce endogeneity.
- Logistic regression to model the *direction* (positive/negative) of returns.

## File Structure

The repository is structured as follows:

- `code/` contains all R scripts used for data cleaning, sentiment computation, data merging, and econometric modeling.
- `datasets/` contains the cleaned datasets used in the analysis, including sentiment scores, price changes, and macroeconomic controls.
- `paper/` contains the final paper, including figures, tables, and the compiled PDF.
