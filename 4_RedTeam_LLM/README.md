# Overview of LLM Vulnerabilities

## LLM Evaluation Misconceptions
First, we need to clarify some common misunderstandings.

* Benchmarks ≠ Safety & Security
* Foundation Model ≠ LLM App

### Benchmarks ≠ Safety & Security
Most benchmarks test performance (like, ARC, Hellaswag, MMLU,..)
<img width="881" alt="image" src="https://github.com/user-attachments/assets/243aa1b5-54ae-428e-b2ab-e46369a841b8">

But Benchmarks don't test safety & security, include:
* Can the model generate offensive orinappropriate sentences?
* Does the model propagate stereotypes?
* Could the model "knowledge" be used fornefarious purposes, e.g. writing malwareor phishing emails?

### Foundation Model ≠ LLM App

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


# Red Teaming Meaning & origin

* Strategy used in cybersecurity and military training
  * A red team simulates adversaries actions andtactics
  * Test and improve the effectiveness of anorganization's defenses
* Red teaming employed to test the robustness, fairness, and ethical boundaries of LLM systems.


# Red Teaming LLM applications

Main Task include:
* Try to bypass safeguards of a givenapplication.
* Find ways to make the bot misbehave like return an inappropriate or incorrect answers to the user





