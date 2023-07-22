---
title: "3.Modeling Information Cascading Behavior Based on Causal Inference (2022.09--2023.02)"
excerpt: "This study employs causal inference to quantify the extent of influence that internal motivation and external environment have on individual decision-making. By delving into the reasons behind individual behavior, it aims to furnish a solid foundation for the formulation of effective policies.<br/><img src='/images/Re_IC_6.png'>"
collection: portfolio
---

Explore causal relationships among variables in an information cascade
---

During the information dissemination process, several factors come into play (using short videos as an example). Elements such as the video publisher's fan count, video duration, tags, and more exert influence on the ultimate scale of information dissemination, including the number of loops, comments, and likes received.

We mainly conduct experiments on the **Bilibili** and **vine** datasets. Each video is a line, including video_id, title, user_name, tag_name, time, description, view, reply, favorite, share, like.... We want to explore the causal relationship between these variables and the magnitude of the causal effect.

**Explore causal graphs using several causal discovery methods:**

No-tears:

<img src='/images/Re_IC_2.png'>

GES: 

<img src='/images/Re_IC_3.png'>

LiNGAM:

<img src='/images/Re_IC_4.png'>


**Calculate causal effects using several causal inference methods:**

When calculating the causal effect, we choose methods that can handle continuous variables, and also try some deep learning-based methods (such as DeepIV, TEDVAE, TARNet, DRNet, VCNet), but cannot get normal output.

**Important insight:**

We found that in the same dataset, the **causal graphs** obtained by different causal discovery methods are **not exactly the same**, and the **causal effects** between variables obtained by different causal inference methods are **not exactly the same**.

From this we have the following question: How to determine the stability boundaries and usage limits of causal discovery and causal inference methods? How to determine the applicable scenarios of different methods? Under the dataset of real scenes, without additional a priori assumptions, is it really possible to use observational data to explore causality?


Understanding the Cascading Behavior of Micro-Individuals
---

Numerous strides have been made in predictive models of information cascades. However, many of these methods are constrained to identifying conventional spreading association patterns, relying solely on correlations within big data. Consequently, they overlook the crucial aspect of whether these models can effectively explain real social phenomena. For instance, when it comes to a particular piece of information, existing methods continue to fall short in providing a comprehensive mechanism and explanation for the intricate dynamics of cascading user participation.

The [RFDID](https://www.sciencedirect.com/science/article/abs/pii/S0306457322000760) incorporates [field dynamic theory](https://psycnet.apa.org/record/2018-46072-001) from social psychology into the study of information cascades, categorizing people's motivation to participate in cascades as internal or external. **Internal motivation** is defined by the similarity between a user's past discourse and the current cascading information, while **external environment** pertains to the user's local social context. Building on this foundation, we delves into the comprehension of cascading behavior in scenarios where information is missing, further enhancing the understanding of the intricate dynamics at play in information cascades.

In many information cascading scenarios, due to privacy policy reasons or technical issues, it is impossible to obtain the user's social relationship or historical speech. Intuitively, if a user has a high degree of awareness of the cascade information but does not participate in the cascade, it can be considered that the external environment has inhibited it. However, if a user has low awareness of the information but participates in the cascade, the environment can be considered to have contributed to it. Conversely, if a user's environment is very positive, but he is not participating in the cascade, it can indicate a low level of intrinsic awareness.

Therefore, when the external environment information is missing, we start from the causal perspective, with the help of the **collider** structure of the **Structural Causal Model**, through the user's internal motivation and cascading participation behavior, to complement the external environment representation. 

The core schematic diagram is as follows:

<img src='/images/Re_IC_6.png'>

