# Video-Summarization-Project

A YouTube video summarization pipeline that:
 Converts video → text using OpenAI Whisper
 Generates summaries using BART, T5, and PEGASUS
 Computes ROUGE evaluation metrics
 Benchmarks latency, inference time, and network-constrained performance
 Visualizes Total Time (Inference + Transmission) vs Bandwidth

# Files
- `Video summarization.ipynb` – This notebook contains the complete end-to-end pipeline for YouTube video summarization. It downloads the video, extracts audio, and performs transcription using Whisper. The generated transcript is then split into manageable chunks, which are summarized using three transformer models — BART, T5, and PEGASUS. The notebook also computes ROUGE-1, ROUGE-2, and ROUGE-L metrics for each model to compare summary quality, followed by a combined evaluation of their performance. Finally, it merges chunk-level summaries into a single coherent output, making this notebook the core processing and evaluation component of the project.

- `result video summarization.ipynb` – This notebook focuses on performance analysis and visualization. It compares the inference time of BART, T5, and PEGASUS, and performs a network-constrained simulation where transmission time is calculated under multiple bandwidth conditions. Using this, it plots the Total Time (Inference + Transmission) vs Bandwidth to understand real-world latency trade-offs. The notebook also displays the final summaries from all three models side-by-side and identifies which model performs best in terms of latency, ROUGE score, and coherence. This file serves as the benchmarking and visualization component of the project.
