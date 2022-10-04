# Early Prediction of Sepsis from Clinical Data

## Table of Contents
- [Abstract](#link-part-1)
- [Design](#link-part-2)
- [Data](#link-part-3)
- [Algorithm](#link-part-4)
- [Tools](#link-part-5)
- [Communication](#link-part-6)
- [**How to run**](#link-part-7)

## <a name="link-part-1">Abstract</a>

Sepsis is a life-threatening condition that occurs when the body's response
to infection causes tissue damage, organ failure, or death ([Singer et al., 2016](https://www.ncbi.nlm.nih.gov/pubmed/26903338)).
In the US, nearly 1.7 million people develop sepsis and 270,000 people die
from sepsis each year; over one third of people who die in US hospitals have
sepsis ([CDC](https://www.cdc.gov/sepsis/datareports/index.html)).

Early detection and antibiotic treatment of sepsis are critical for improving
sepsis outcomes, where each hour of delayed treatment has been associated with
roughly an 4-8% increase in mortality. The goal of the project is early detection
of sepsis using physiological data.

## <a name="link-part-2">Design</a>

This project comes from the [PhysioNet/Computing in Cardiology Challenge](https://physionet.org/content/challenge-2019/1.0.0/)
in 2019. The data is sourced from ICU patients in three separate hospital systems.
Classifying sepsis label to take action in the early phase of sepsis before getting
server.


## <a name="link-part-3">Data</a>

Get the dataset by running this command:
```
wget -r -N -c -np https://physionet.org/files/challenge-2019/1.0.0/
```

The data contains 40,336 files and each file contains a table providing a sequence
of measurements over time. Each row represents a single hour's worth of data. There
are 41 columns including vital signs, laboratory values, Demographics, and the target
outcome.

## <a name="link-part-4">Algorithm</a>

**Data Cleaning:**

1. Removing columns with a missing rate higher than 93%.
2. Filling NaN HR, Temp, SBP, Resp, O2Sat and MAP values with the last non-NaN value.
3. Marking the rest NaN values as "missing".

**Feature Engineering:**

1. Getting the symptoms of sepsis.
2. Creating labels for HR, Age, Temp, Resp, SBP, MAP and DBP columns.

**Models:**

I've tried logistic regression, random forest and bagging classifiers, and as a result,
bagging classifier outperform the others which is the final model I used.

**Model Evaluation and Selection:**

The dataset was split into 80/20 train vs. heldout, and all scores reported was calculated using the
[TestKit](/testing.ipynb). It counts as true positive result if the classifier predicts
sepsis between 12 hours before and 3 hour after sepsis time, which in this case is between
6 hours before and 9 hours after SepsisLabel turns into 1.

**Final bagging scores:** 18 features
- Accuracy: 

## <a name="link-part-5">Tools</a>

* **Pandas** for exploratory data analysis.
* **Matplotlib** and **Seaborn** for plotting.
* **Scikit Learn** for modeling.
* **Pickle** for saving models in a pickle file.

## <a name="link-part-6">Communication</a>

The project proposal is shown [here](/documents/proposal.md).

The MVP document is shown [here](/documents/MVP.md).

## <a name="link-part-7">How to run</a>

Get the model by running [random_forest.ipynb](/models/random_forest.ipynb).

Test the model by running [testing.ipynb](/testing.ipynb).
