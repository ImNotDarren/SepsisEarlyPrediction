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

## <a name="link-part-2">Design</a>



## <a name="link-part-3">Data</a>

Get the dataset by running this command:
```
wget -r -N -c -np https://physionet.org/files/challenge-2019/1.0.0/
```

## <a name="link-part-4">Algorithm</a>



## <a name="link-part-6">Communication</a>

The project proposal is shown [here](/documents/proposal.md).

The MVP document is shown [here](/documents/MVP.md).

## <a name="link-part-7">How to run</a>
Get the model by running [random_forest.ipynb](/models/random_forest.ipynb).
Test the model by running [testing.ipynb](/testing.ipynb).
