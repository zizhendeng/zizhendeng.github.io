---
title: "1.Causal Alignment for Large Language Models"
excerpt: "We propose a novel approach based on causal abstraction theory and mixture of experts to find the neural representation corresponding to a given causal variable in the causal structure model."
collection: portfolio
---

Existing interpretability tools are often incapable of adapting to large language models with hundreds of millions of parameters, as they tend to focus on small models fine-tuned for specific tasks. In this study, we propose a novel approach based on causal abstraction theory and mixture of experts to find the neural representation corresponding to a given causal variable in the causal structure model. The highlights are as follows:

1.Introduce the intervention operation in the causal inference into the large language model, use different designed inputs to achieve soft intervention on intermediate variables, and train through the loss between the actual output and the model output to align the neural representation in the large language model with the variables in the causal model.

2.To our knowledge, this work is the first to use mixture of experts for causal alignment of large language models, exploring the disentangle function of mixture of experts models nonlinearly separating high-dimensional semantic causal variables in neural representations, aligning with human cognition, So as to better understand the operating mechanism of the large language model.
