# Parameter Efficient Fine Tuning: Gemma

This is a short notebook tutorial designed to introduce fine tuning on [Google's Gemma model](https://huggingface.co/google/gemma-7b). 

## Overview

The goal of this tutorial is not to make you an expert at fine-tuning, but rather show you how easy it is to fine-tune a sophisticated model on new data. Use the code in this tutorial as a guide for your specific application.

## Why Fine Tune? 

Large Language Models (LLMs) are very capable. However, they are often not specialized enough for specific tasks, such as generating scientific or medical information. Rather than train the entire model from scratch, we can make use of what the model already knows (language/writing skills, general knowledge, etc.) and train the model at its current state. This is called fine-tuning, where we start with a pre-trained general model and train it on data for a specific task. 

## Getting Started

To access Gemma for this tutorial, you need a [HuggingFace](www.huggingface.co) account and a HuggingFace API Token with write permissions (In HF: Profile -> Settings -> Access Tokens). Additionally, you need to visit [Gemma's HuggingFace Space](https://huggingface.co/google/gemma-7b) and click the button to accept their terms of use. After accepting the terms, access should be immediately granted.

## Libraries

We are going to be using several libraries found often in deep learning pipelines. 

- **Transformers**: library by HuggingFace for publishing, accessing, and training models
- **Datasets**: library by HuggingFace for publishing and accessing datasets
- **Accelerate**: library by HuggingFace for accelerated model training

## The Dataset

In this tutorial we will be using the [English Quotes Dataset](https://huggingface.co/datasets/Abirate/english_quotes) from HuggingFace. This is a dataset containing quotes and their authors. We are going to train Gemma to, given a quote beginning, complete the quote and list its author.  
