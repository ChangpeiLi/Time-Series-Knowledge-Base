# ChatTS Key Code

## generate_llm_qa.py
Core script for generating time-series question-answer training data.

Main pipeline:

Metric / Domain Selection
→ Controlled Attribute Generation
→ Synthetic Time-Series Generation
→ Time-Series Encoding
→ Prompt Construction
→ LLM-based QA Generation
→ QA Parsing
→ Dataset Saving

Main functions:
- generate_prompt_data()
- generate_dataset()

Key dependencies:
- chatts.ts_generator.generate
- chatts.utils.llm_utils
- chatts.utils.encoding_utils
- chatts.utils.attribute_utils
