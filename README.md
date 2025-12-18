# R-Ollama-Lab

📖 **[View the Interactive Guide](https://ahjavid.github.io/R-Ollama-Lab/)**

A practical guide for using local LLMs with R for biostatistics and data analysis using the [ollamar](https://hauselin.github.io/ollama-r/) package.

## Overview

This repository provides templates and workflows for integrating local Large Language Models (via Ollama) into biostatistics workflows, including:

- **Statistical Consultation** - Get expert advice on methods and tests
- **R Code Generation** - Generate analysis code with proper parameters
- **Iterative Analysis Design** - Build complex analyses step-by-step
- **Literature Search** - Semantic search using embeddings
- **Structured Outputs** - JSON schema responses for reports
- **Parallel Processing** - Efficient batch queries

## Features

- 🎨 **Styled LLM Output Boxes** - Clean, visually appealing response formatting
- 📝 **Markdown Rendering** - LLM responses render with proper formatting (bold, lists, headers)
- 🔧 **Flexible Helper Functions** - `ask_expert()` and `generate_code()` with customizable parameters
- 📊 **Real Data Examples** - Hands-on demos using built-in R datasets

## Prerequisites

1. **Install Ollama** from [ollama.com](https://ollama.com)
2. **Install R packages**:
   ```r
   install.packages("ollamar")
   ```

## Recommended Models

| Model | Size | Best Use | Speed |
|-------|------|----------|-------|
| `qwen3:14b` | 9.3GB | R code generation, complex analysis | ⚡⚡ |
| `gemma3:12b` | 8.1GB | Complex reasoning, study design | ⚡⚡ |
| `qwen3:4b` | 2.5GB | Quick code questions | ⚡⚡⚡ |
| `gemma3:4b` | 3.3GB | Fast reasoning, general tasks | ⚡⚡⚡ |
| `phi4-mini:3.8b` | 2.5GB | Efficient general-purpose | ⚡⚡⚡ |
| `granite4:3b` | 2.1GB | IBM's enterprise model | ⚡⚡⚡ |
| `llama3.2:3b` | 2.0GB | Fast explanations, summaries | ⚡⚡⚡ |
| `nomic-embed-text-v2-moe` | 957MB | Embeddings, semantic search | ⚡⚡⚡ |
| `mxbai-embed-large` | 669MB | Embeddings, literature search | ⚡⚡⚡ |

### Pull Models

```bash
# Primary models
ollama pull qwen3:14b        # Best for R code
ollama pull gemma3:12b       # Best for reasoning

# Fast alternatives
ollama pull gemma3:4b
ollama pull llama3.2:3b

# Embeddings
ollama pull mxbai-embed-large
```

## Quick Start

1. Start Ollama
2. Open `Ollama_Biostatistics_Practical.Rmd` in RStudio
3. Set `run_llm <- TRUE` in the setup chunk
4. Knit the document or run chunks interactively

## Files

- `Ollama_Biostatistics_Practical.Rmd` - Main practical guide with examples
- `index.html` - Rendered HTML for GitHub Pages

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

```bibtex
@article{Lin2025,
  author = {Lin, Hause and Safi, Tawab},
  title = {ollamar: An R package for running large language models},
  journal = {Journal of Open Source Software},
  volume = {10},
  number = {105},
  pages = {7211},
  year = {2025},
  doi = {10.21105/joss.07211}
}
```

## Resources

- [ollamar documentation](https://hauselin.github.io/ollama-r/)
- [Ollama model library](https://ollama.com/library)
- [ollamar GitHub](https://github.com/hauselin/ollama-r)

## License

MIT License
