# R-Ollama-Lab

A practical guide for using local LLMs with R for biostatistics and data analysis using the [ollamar](https://hauselin.github.io/ollama-r/) package.

## Overview

This repository provides templates and workflows for integrating local Large Language Models (via Ollama) into biostatistics workflows, including:

- **Statistical Consultation** - Get expert advice on methods and tests
- **R Code Generation** - Generate analysis code with proper parameters
- **Iterative Analysis Design** - Build complex analyses step-by-step
- **Literature Search** - Semantic search using embeddings
- **Parallel Processing** - Efficient batch queries

## Prerequisites

1. **Install Ollama** from [ollama.com](https://ollama.com)
2. **Install R packages**:
   ```r
   install.packages("ollamar")
   ```

## Recommended Models

| Model | Size | Best Use | Speed |
|-------|------|----------|-------|
| `qwen2.5-coder:7b` | 4.7GB | R code, data analysis | ⚡⚡ |
| `qwen2.5-coder:3b` | 1.9GB | Quick questions | ⚡⚡⚡ |
| `gemma3n:e4b` | 7.5GB | Complex reasoning | ⚡⚡ |
| `qwen3-vl:8b` | 6.1GB | Vision, plot critique | ⚡⚡ |
| `ministral-3:8b` | 6.0GB | Study design, reasoning | ⚡⚡ |
| `llama3.2:3b` | 2.0GB | Explanations | ⚡⚡⚡ |
| `mxbai-embed-large` | 669MB | Literature search | ⚡⚡⚡ |

### Pull Models

```bash
ollama pull qwen2.5-coder:7b
ollama pull gemma3n:e4b
ollama pull qwen3-vl:8b
ollama pull ministral-3:8b
ollama pull llama3.2:3b
ollama pull mxbai-embed-large
```

## Quick Start

1. Start Ollama
2. Open `Ollama_Biostatistics_Practical.Rmd` in RStudio
3. Set `run_llm <- TRUE` in the setup chunk
4. Knit the document or run chunks interactively

## Files

- `Ollama_Biostatistics_Practical.Rmd` - Main practical guide with examples

## Use Cases

### Sample Size & Power Calculations
```r
generate_code("Calculate sample size for 2-arm RCT...")
```

### Survival Analysis
```r
generate_code("Create Kaplan-Meier curves and Cox regression...")
```

### Missing Data Strategy
```r
ask_expert("Recommend MMRM vs MI for longitudinal trial...")
```

### Propensity Score Analysis
```r
generate_code("Complete PS analysis with MatchIt...")
```

## Citation

If you use ollamar, please cite:

```
Lin, H., & Safi, T. (2025). ollamar: An R package for running large 
language models. Journal of Open Source Software, 10(105), 7211. 
https://doi.org/10.21105/joss.07211
```

## Resources

- [ollamar documentation](https://hauselin.github.io/ollama-r/)
- [Ollama model library](https://ollama.com/library)
- [ollamar GitHub](https://github.com/hauselin/ollama-r)

## License

MIT License
