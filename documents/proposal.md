# Project Proposal

## Question/Need:

This project comes from the [PhysioNet/Computing in Cardiology Challenge](https://physionet.org/content/challenge-2019/1.0.0/)
in 2019.

Sepsis is a life-threatening condition that occurs when the body's response
to infection causes tissue damage, organ failure, or death ([Singer et al., 2016](https://www.ncbi.nlm.nih.gov/pubmed/26903338)).
In the US, nearly 1.7 million people develop sepsis and 270,000 people die
from sepsis each year; over one third of people who die in US hospitals have
sepsis ([CDC](https://www.cdc.gov/sepsis/datareports/index.html)).

Early detection and antibiotic treatment of sepsis are critical for improving
sepsis outcomes, where each hour of delayed treatment has been associated with
roughly an 4-8% increase in mortality. The goal of the project is early detection
of sepsis using physiological data.

## Data Description:

The data I used is sourced from ICU patients in three separate hospital systems.
It includes 40,336 files and each file contains a table providing a sequence of
measurements over time. There are 41 columns including vital signs, laboratory
values, Demographics, and the target outcome.

## Tools:

* **Pandas** for exploratory data analysis.
* **Matplotlib** and **Seaborn** for plotting.
* **Scikit Learn** for modeling.
* **Pickle** for saving models in a pickle file.

## MVP Goal:
My MVP goal is to analysing the data to build some virtualizations and determine
which classification method to use.
