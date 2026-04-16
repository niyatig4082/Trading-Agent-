**AI Trading Agent with LLM-Based Decision System**
Overview 
This project implements an end-to-end AI trading agent that leverages Large Language Models (LLMs) to make data-driven investment decisions in a simulated real-time environment.

[Developed as part of graduate-level Natural Language Processing (NLP) coursework at Worcester Polytechnic Institute (WPI).]

The system integrates structured financial signals with unstructured data and performs multi-step reasoning to generate actionable trading decisions.

Key Features
🤖 LLM-Based Decision Making
Uses transformer-based models to analyze market conditions and generate buy/sell/hold decisions.
🔧 Tool-Calling Framework
Integrates multiple data sources:
Market news & sentiment
Technical indicators (RSI, MACD)
Historical price data
🧠 Memory Module (BM25 Retrieval)
Stores past trading experiences and retrieves similar scenarios to inform future decisions.
📊 Backtesting Engine
Evaluates trading strategies across multiple iterations to measure performance.
🏷️ Auto-Labeling Pipeline
Generates training data by labeling trades based on profit/loss outcomes.

🏗️ System Architecture
State Collection – Fetches market data (news, indicators, prices)
Context Enrichment – Adds relevant historical memory using BM25 retrieval
LLM Decision Layer – Performs multi-step reasoning using tool calls
Execution Layer – Simulates trades and updates portfolio
Learning Pipeline – Logs interactions → labels outcomes → fine-tunes model

🧪 Model Training
Fine-tuned transformer-based models using:
LoRA (Low-Rank Adaptation)
Explored QLoRA-style quantization techniques
Custom dataset (sft_data.jsonl) generated from trading interactions
Prompt-completion formatting with label masking for supervised fine-tuning

📂 Data & Memory
Trading Data: sft_data.jsonl (prompt, decisions, PnL-based labels)
Memory System: trading_memory.json using BM25 retrieval

⚠️ Challenges & Learnings
Handling noisy and multilingual LLM outputs
Managing token length limitations in long-context reasoning
Working without clean ground truth labels

Bridging the gap between:

“Works in a notebook” vs. “Works as a system”

🚀 Future Improvements
Improve evaluation metrics for decision quality
Incorporate reinforcement learning
Expand memory for long-term learning
Optimize for real-time deployment
🛠️ Tech Stack
Python, PyTorch
Hugging Face Transformers
LoRA / QLoRA
BM25 (rank_bm25)
Pandas, NumPy
Alpha Vantage, yfinance

📌 Author
Niyati Gohil
MS Data Science, Worcester Polytechnic Institute (WPI)

⭐ Why This Project
This project demonstrates the application of NLP and LLM techniques in real-world decision systems, combining language understanding, structured data integration, and iterative learning pipelines.
