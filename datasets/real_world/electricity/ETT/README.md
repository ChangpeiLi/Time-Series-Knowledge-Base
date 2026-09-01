# ETT Dataset

ETT stands for Electricity Transformer Temperature.

It contains four subsets:

- ETTh1
- ETTh2
- ETTm1
- ETTm2

## Basic Information

| Dataset | Variables | Sampling Frequency | Number of Time Steps |
|---|---:|---|---:|
| ETTh1 | 7 | 1 hour | 17,420 |
| ETTh2 | 7 | 1 hour | 17,420 |
| ETTm1 | 7 | 15 minutes | 69,680 |
| ETTm2 | 7 | 15 minutes | 69,680 |

## Description

The ETT datasets record electricity transformer temperature and related load features.

- `ETTh1` and `ETTh2` are sampled hourly.
- `ETTm1` and `ETTm2` are sampled every 15 minutes.
- Each dataset contains 7 variables.
- `OT` is commonly used as the oil-temperature target variable.

## Usage

ETT is widely used for long-term time-series forecasting and is frequently used in the papers studied in this project.

## Source

Original dataset:
Zhou et al., ETT Dataset

Official repository:
https://github.com/zhouhaoyi/ETDataset
