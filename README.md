# Parameter Efficient Fine Tuning: Gemma

This is a short notebook tutorial designed to introduce fine tuning on [Google's Gemma model](https://huggingface.co/google/gemma-7b). 


## Why Fine Tune? 

Large Language Models (LLMs) are very capable. However, they are often not specialized enough for specific tasks, such as generating scientific or medical information. Rather than train the entire model from scratch, we can make use of what the model already knows (language/writing skills, general knowledge, etc.) and train the model at its current state. This is called fine-tuning, where we start with a pre-trained general model and train it on data for a specific task. 
