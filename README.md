---
library_name: peft
---
This repository contains code for fine-tuning a Llama 2 chatbot model using QLoRA, a technique for efficient parameter-efficient fine-tuning. The project leverages the Hugging Face Transformers library and the bitsandbytes library to load and train the model in 4-bit precision.
By fine-tuning the pre-trained Llama 2 model on a curated dataset of instructions and responses, this project aims to improve the model's ability to follow instructions and generate coherent, contextually relevant text.
The resulting fine-tuned chatbot model can be used for various conversational AI tasks, such as answering questions, generating text, and engaging in dialogue.
Key features:
- Utilizes the QLoRA method for parameter-efficient fine-tuning.
- Employs 4-bit precision training for reduced memory footprint and faster training.
- Leverages the Hugging Face Transformers library for seamless integration.
- Includes a text generation pipeline for easy interaction with the fine-tuned model.

## Training procedure


The following `bitsandbytes` quantization config was used during training:
- load_in_8bit: False
- load_in_4bit: True
- llm_int8_threshold: 6.0
- llm_int8_skip_modules: None
- llm_int8_enable_fp32_cpu_offload: False
- llm_int8_has_fp16_weight: False
- bnb_4bit_quant_type: nf4
- bnb_4bit_use_double_quant: False
- bnb_4bit_compute_dtype: float16
### Framework versions


- PEFT 0.4.0
