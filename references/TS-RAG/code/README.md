# TS-RAG Key Code

This folder contains the key source files related to time-series retrieval and retrieval-augmented forecasting in TS-RAG.

## Code Map

### retrieve.py
Core retrieval pipeline.

Main functions:
- Slice raw time series using sliding windows
- Convert time-series slices into embeddings
- Build and save the retrieval database
- Build FAISS index
- Calculate L2 similarity
- Perform Top-K retrieval

Main pipeline:

Raw Time Series
→ Sliding Window Slicing
→ Time-Series Embedding
→ Retrieval Database
→ FAISS Index
→ Similarity Search
→ Top-K Retrieved Sequences


### ChronosBolt.py
Core forecasting model and retrieval augmentation model.

Main functions:
- Instance normalization
- Time-series patching
- Input patch projection
- T5 Encoder
- Retrieval sequence encoding
- Attention and gating based retrieval fusion
- Forecast generation


### zeroshot.py
Zero-shot forecasting entry point.

Main functions:
- Load embedding model
- Call retrieval pipeline
- Load retrieved sequences
- Load Chronos-Bolt with retrieval
- Perform retrieval-augmented zero-shot forecasting


### dataset.py
Dataset organization for pre-training.

Main functions:
- Construct context and prediction samples
- Load retrieval indices and distances
- Build FAISS index for pre-training retrieval


### pretrain.py
Training pipeline for retrieval-augmented models.

Main functions:
- Load Chronos-Bolt with retrieval
- Load retrieved historical sequences
- Fuse retrieved sequences with current input
- Calculate loss and update retrieval augmentation modules
