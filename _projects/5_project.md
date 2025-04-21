---
layout: page
title: Extending SecureLLM using Advanced Finetuning Methods
description: >
    Security is an incredibly important issue that exists in the current LLM scene. Any practical use case of an LLM that includes databases with multiple access levels introduces a possible security risk to the system. While multiple works providing possible methods to ’detoxify’ or add guardrails to LLMs exist, those methods can provide no provable guarantee of not leaking data. We extend on our prior published work, SecureLLM, which is an approach that guarantees security with no data leakage by composing appropriate fine-tuned models. The power of SecureLLM relies heavily on the fine-tuned models used for composition, thus we present a thorough analysis and benchmarking of several widespread LLM fine-tuning techniques, highlighting strengths and weaknesses of the approach compared to an insecure generalized model trained on all the data which acts as an upper bound in performance. We present results showing that our SecureLLM composition can get close to the performance of the generalized model and sometimes match it under a distributional shift.
img: assets/img/SECURELLM.png
importance: 5
---
