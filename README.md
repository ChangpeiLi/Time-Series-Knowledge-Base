# Time-Series-Knowledge-Base

A knowledge base for time-series retrieval, time-series question answering, and related datasets.

This repository mainly organizes the key code and datasets related to two core reference methods:

- TS-RAG
- ChatTS

The current research focuses on combining time-series retrieval with ChatTS-based time-series question answering.

## Repository Structure

Time-Series-Knowledge-Base/

- references/
  - TS-RAG/
    - code/
  - ChatTS/
    - code/
- datasets/
  - synthetic/
  - real_world/
    - electricity/
      - ETT/
      - ECL/
      - Solar-Energy/

## References

### TS-RAG

TS-RAG is mainly used as the reference for time-series retrieval and retrieval-augmented forecasting.

Key topics include:

- Time-series slicing
- Time-series embedding
- Retrieval database construction
- FAISS similarity search
- Top-K retrieval
- Retrieval augmentation

Key code:

- `retrieve.py`
- `ChronosBolt.py`
- `zeroshot.py`

Location:

`references/TS-RAG/`

### ChatTS

ChatTS is mainly used as the reference for time-series understanding and time-series question answering.

Key topics include:

- Controlled time-series attribute generation
- Synthetic time-series generation
- Time-series textual description
- Time-series QA generation
- LLM-based training data generation

Key code:

- `generate.py`
- `generate_llm_qa.py`

Location:

`references/ChatTS/`

## Datasets

### Synthetic Data

The synthetic dataset section is used to organize time series with controlled characteristics, including:

- Trend
- Periodicity
- Noise
- Upward and downward spikes
- Continuous anomalies
- Sudden changes
- Other local patterns

Location:

`datasets/synthetic/`

### Real-World Electricity / Energy Data

#### ETT

The ETT family contains:

- ETTh1
- ETTh2
- ETTm1
- ETTm2

The four CSV files are stored directly in this repository.

Location:

`datasets/real_world/electricity/ETT/`

#### Electricity / ECL

The hourly ECL dataset contains 321 electricity-consumption time series.

Because the official TSF file is too large for convenient direct upload through the GitHub web interface, the repository provides dataset information and the official download source in its README.

Location:

`datasets/real_world/electricity/ECL/`

#### Solar-Energy

The Solar-Energy dataset contains 137 solar power generation time series sampled every 10 minutes.

The official TSF dataset file is stored directly in this repository.

Location:

`datasets/real_world/electricity/Solar-Energy/`

## Current Research Direction

The current research direction is mainly based on ChatTS and TS-RAG.

TS-RAG provides the reference for time-series knowledge-base construction and retrieval, while ChatTS provides the reference for time-series natural-language question answering.

The planned research pipeline is:

Current Time Series  
→ Time-Series Slicing  
→ Time-Series Embedding  
→ Similarity Retrieval  
→ Top-K Historical Time-Series Retrieval  
→ Retrieved Knowledge / QA Context  
→ Prompt Construction  
→ ChatTS  
→ Time-Series Question Answering

The repository will continue to be extended as the experimental work progresses.
