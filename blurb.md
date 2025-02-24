I have worked on multiple aspects of evaluating, improving and formally guaranteeing security, privacy and reliability of deep learning enabled AI systems: 

1. My recent focus has been on safety/security for agentic AI systems. We are currently building an attack based security evaluation framework for agents on top of browsergym. We also built an internal red teaming tool exposing security vulnerabilities of ServiceNow's AI offerings and are working on mitigations to address these.

2. I have developed several attacks that expose previously unknown vulnerabilities of AI systems. The most recent one involves stealthy fine tuning attacks that were validated against production fine tuning APIs of several leading LLM providers (currently under responsible disclosure and awarded a bug bounty award). Last year, we showed that production grade LLM APIs can be used to steal parts of closed source models, that won a best paper award at ICML 2024.

3. I led the adversarial testing efforts (report Section 9)  for the Gemini 1.5 family of models, evaluating Gemini for vulnerabilities to jailbreaking and prompt injection attacks 

4. Previously, I worked a lot on provable robustness guarantees against adversarial attacks on deep learning systems, with some highlights being in this framework (an earlier version of which was productionized on the Google play store to improve robustness of text classifiers for detecting fraudulent apps against adversarial attacks) and this work that was, at the time of publication, the SOTA in provable robustness guarantees against norm bounded adversarial attacks. We are currently working on extending these approaches to VLMs, particularly those that use inference time reasoning/thinking. 

5. I also developed this work that achieves the current SOTA tradeoff between memory and performance on Google's differentially private federated learning system (see here).

6. I have also worked on human-AI collaboration and its implications for alignment, including this work that showed state of the art results by combining Google's medical image AI systems with human clinicians. I also contributed to this work on richer feedback for t2i models that won a best paper at CVPR 2024.
