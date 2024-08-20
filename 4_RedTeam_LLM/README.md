# What's LLM RedTeaming
An important part of secure delivery software is red team testing, which broadly refers to the practice of simulating real-world adversaries and their tools, strategies, and programs to identify risks, discover blind spots, validate hypotheses, and improve the overall security status of the system.

The practice of artificial intelligence red team testing has developed to have a broader meaning, including：

* Detecting security vulnerabilities
* Detecting other system failures, such as generating potentially harmful content

The intersection and differences between AI red teams and traditional red teams are：

* **The scope of the AI Red Team is broader**. The AI Red Team is now a general term for detecting safety and RAI(responsible AI) results. The AI red team intersects with traditional red team targets, for example, some targets may include stealing underlying models. But AI systems also inherit new security vulnerabilities, such as prompt injection and poisoning, which require special attention. In addition to safety objectives, the AI Red Team also includes detecting fairness issues (such as stereotyping) and harmful content (such as glorifying violence) as results. The AI Red Team helps to detect these issues early.

* **AI Red Team testing focuses on unexpected outcomes that may arise from malicious and legitimate users**. The AI Red Team test not only focuses on how malicious opponents can disrupt AI systems through security techniques and vulnerabilities, but also on how the system generates problematic and harmful content when interacting with ordinary users. Therefore, unlike traditional security red team testing that primarily focuses on malicious opponents, AI red team testing considers a wider range of roles and failures.

* **AI systems are constantly evolving**. AI applications often undergo changes. For example, in large language model applications, developers may modify the meta prompt (prompt code) based on feedback. Although traditional software systems may also undergo changes, the speed of change in AI systems is faster. Therefore, it is important to conduct multiple rounds of red team testing on the AI system and establish an automated measurement and monitoring system for the system over time.

* **The red team generative AI system requires multiple attempts**. In traditional red team exercises, using tools or techniques on the same input at two different time points always produces the same output. In other words, traditional red team exercises are generally deterministic. Generative AI systems, on the other hand, are probabilistic. This means that running the same input twice may produce different outputs. This is due to design, as the probabilistic nature of generative AI allows for a wider range of creative outputs. This also makes the Red Team exercise tricky, as prompts may not lead to failure in the first attempt, but will achieve success in subsequent attempts.

* **Mitigating AI failures requires deep defense**. Just as in traditional security, issues such as phishing require various technical mitigation measures (such as strengthening hosts to intelligently identify malicious URL or attachments that contains malicious virus), fixing faults discovered through AI red teams also requires a defense in depth approach. This involves techniques such as "using classifiers to label potentially harmful content" and "using metapromps to guide behavior", alternatively, input and output security risks can be addressed by integrating LLM Guard Protection.

The following figure is based on the development trend of ubiquitous artificial intelligence and describes the specific scope of the Red Team's work.
![image](https://github.com/user-attachments/assets/a23c9dd5-2771-49fe-a861-6379c206ccf7)

In general, the meaning of Red Teaming is:

* A strategy used in cybersecurity and military training
  * A red team simulates adversaries actions andtactics
  * Test and improve the effectiveness of anorganization's defenses
* A job which employed to test the robustness, fairness, and ethical boundaries of LLM systems.
* A goal which aiming to break into the system and try to bypass safeguards of a givenapplication.



# Difference between RedTeaming and Evaluation Benchmarks
First, we need to clarify some common misunderstandings.

**Benchmarks ≠ Safety & Security**
Most benchmarks test performance (like, ARC, Hellaswag, MMLU,..)
<img width="881" alt="image" src="https://github.com/user-attachments/assets/243aa1b5-54ae-428e-b2ab-e46369a841b8">

But Benchmarks don't test safety & security, include:
* Can the model generate offensive orinappropriate sentences?
* Does the model propagate stereotypes?
* Could the model "knowledge" be used fornefarious purposes, e.g. writing malwareor phishing emails?



# What are the RedTeam's main focus
* Foundation Model
* LLM Application

LLM application shared risks with Foundation Model:
* Toxicity & offensive content
* Criminal & illicit activities
* Bias & stereotypes
* Privacy & data security

But LLM application unique risks:
* Inappropriate content
* Out of scope behavior (like ssrf with plugins.)
* Hallucinations
* Sensitive information disclosure (with prompt injection)
* Security vulnerabilities

