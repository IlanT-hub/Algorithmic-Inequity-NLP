# Algorithmic-Inequity-NLP

I evaluate how underrepresentation in training data produces diagnostic failures in clinical natural language processing. This repository contains the tools and research used to identify a 36 percent recall gap in minority patient narratives.

Project Overview

The core of this work is a diagnostic sensitivity audit. I used a Python 3.10 script to test Gemini 2.5 Flash against clinical stories from the MIMIC III database. I identified that the model responds to identity markers instead of physical lung symptoms. This creates an intensity gap in care recommendations.

Getting Started

Create a Python 3.10 environment.

Install the requests library using your terminal.

Obtain a Google Generative AI API key.

Place your API key in the configuration section of the script located in /src.

Run the script to reproduce the audit findings.

The audit uses zero shot inference with a temperature of zero. This ensures the results are deterministic and reproducible.

Repository Structure

/paper: Contains the final  research paper.
/src: Holds the Python audit script used to quantify the performance collapse.
/visuals: Includes the charts and graphs that support the research claims.
/data: Descriptions of the MIMIC-III v1.4 datasets used in the study.

Technical Metrics

I measure success using Precision Recall and the F1 Score. I used a Chi squared test of independence to verify the statistical significance of my results. The findings suggest that data augmentation improves minority cohort performance by 15 percent.

Reference

This work is part of a senior capstone project on medical AI safety and linguistic equity.
