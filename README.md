# Fine-tuning-an-LLM-for-Academic-writing
Fine-tuning the TinyLLaMA model to generate short summaries of research papers, and enhancing these short summaries by formatting them into structured research paper summaries using the Gemini 1.5 Flash model.

## Features
- Fine-tuned TinyLLaMA-1.1B using LoRA and PEFT
- Integration with Gemini 1.5 Flash API for structured formatting
- Processes 10,000 records selected from a 41,000-record arXiv dataset
- Gradio-based user interface for easy input/output

## Dataset Details

- **Source**: Kaggle – https://www.kaggle.com/datasets/neelshah18/arxivdataset/data
- **Total Records**: ~41,000
- **Training Subset**: 10,000 records (selected due to memory limits)
- **Key Fields Used**:
  - `Title`: Research paper title
  - `Summary`: Concise paper summary or abstract
- **Other Fields**: Author, Year, Month, Date, Link (not used)

## Objective

The primary objective is to create an AI-driven tool that generates **structured summaries of research papers** based on user-provided titles. The system emphasizes:
- Concise academic summaries
- Structured outputs with:  
  `Title | Introduction | Objective | Summary | Conclusion`
- Efficient model training using **LoRA** and **PEFT**
- Compatibility with **Google Colab T4 GPU**

## Model Workflow

1. **Input**: User provides the **title** of a research paper.
2. **TinyLLaMA-1.1B**: Generates a short 200-word summary using the fine-tuned model.
3. **Gemini 1.5 Flash API**: Enhances and formats the summary into structured sections:
   - Title  
   - Introduction  
   - Objective  
   - Summary  
   - Conclusion
4. **Gradio UI**: Displays the final structured summary for the user.
