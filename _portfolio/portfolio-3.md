---
title: "3.Modeling Information Cascading Behavior Based on Causal Inference"
excerpt: "This study uses causal inference to calculate the degree of influence of internal motivation and external environment on individual decision-making, understand the reasons behind individual behavior, and provide a basis for policy formulation."
collection: portfolio
---

Exploring causal relationships among variables in an information cascade
---

In the process of dissemination of information, there are many factors (taking short videos as an example, such as the number of fans of the video publisher, video duration, tags, etc.) that will affect the final scale of information dissemination (number of loops, comments, likes).

We mainly conduct experiments on the Bilibili and vine datasets. Each video is a line, including video_id, title, user_name, tag_name, time, description, view, reply, favorite, share, like.... We want to explore the causal relationship between these variables and the magnitude of the causal effect.

**Explore causal graphs using several causal discovery algorithms:**

PC:
<img src='/images/Re_IC_1.png'>

No-tears:
<img src='/images/Re_IC_2.png'>

GES: 
<img src='/images/Re_IC_3.png'>

LiNGAM:
<img src='/images/Re_IC_4.png'>

Gran-DAG: 
<img src='/images/Re_IC_5.png'>

**Calculate causal effects using multiple causal inference methods:**

When calculating the causal effect, we choose methods that can handle continuous variables, and also try some deep learning-based methods (such as DeepIV, TEDVAE, TARNet, DRNet, VCNet), but cannot get normal output.

**Important insight:**

We found that in the same dataset, the causal graphs obtained by different causal discovery methods are not exactly the same, and the causal effects between variables obtained by different causal inference methods are not exactly the same.

From this we have the following question: how to use the information itself (unstructured data, text and video) to explore causality? How to determine the stability boundaries and usage limits of causal discovery and causal inference methods? How to determine the applicable scenarios of different methods? Under the dataset of real scenes, without additional a priori assumptions, is it really possible to use observational data to explore causality?


Understanding the Cascading Behavior of Micro-Individuals
---

Many milestones have been achieved in predictive models of information cascades, but most of these methods are limited to identifying common spreading association patterns relying on the correlations of big data, ignoring whether the proposed models can explain well actual social phenomena. For example, for a specific piece of information, the existing methods still cannot give a detailed mechanism and explanation of the cascading user participation.

Research [xxx] introduces the field dynamic theory [xxx] in social psychology into information cascade, and divides people's motivation to participate in the cascade into internal cognition and external motivation. Intrinsic cognition is characterized by the similarity between the user's historical speech and current cascading information, and extrinsic motivation is represented by the user's local social environment. On this basis, we further consider the understanding of cascading behavior under the condition of missing information.

In many information cascading scenarios, due to privacy policy reasons or technical issues, it is impossible to obtain the user's social relationship or historical speech. Intuitively, if a user has a high degree of awareness of the cascade information but does not participate in the cascade, it can be considered that the external environment has inhibited it. However, if a user has low awareness of the cascade but participates in the cascade, the environment can be considered to have contributed to it. Conversely, if a user's environment is very positive, but he is not participating in the cascade, it can indicate a low level of intrinsic awareness.

Therefore, when the external environment information is missing, we start from the causal perspective, with the help of the collision structure of the structural causal model, through the user's internal cognition and cascading participation behavior, to complement the external environment representation. Or complement the internal cognition according to the external environment and cascading conditions. Then a complete internal cognition and external environmental strength can be obtained, so as to understand the reason why the individual participates in the cascade.

The core schematic diagram is as follows:

<img src='/images/Re_IC_6.png'>

