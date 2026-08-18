# Receiver Inference in Relational Event History Data  
## Reconstructing Communication Networks with Large Language Models

This repository contains the code accompanying the paper:

> *Receiver Inference in Relational Event History Data: Reconstructing Communication Networks with Large Language Models*

The project focuses on inferring **message addressees (receivers)** in multi-party conversations—specifically parliamentary debates—using large language models (LLMs), and evaluating the resulting communication networks.

---

## Overview

Relational Event History (REH) datasets often include information about **who speaks**, but lack explicit information about **who is being addressed**. This repository provides a framework to:

- Infer receivers using an API  
- Construct directed communication networks  
- Evaluate predictions at both the **turn level** and **network level**  
- Analyze model confidence and uncertainty
- Conduct Relational Event Model (REM) analyses on the resulting interaction data 

The implementation is applied to Dutch parliamentary debate transcripts and supports both receiver inference and downstream relational event analysis.

---

## Repository Structure
```text
├── Prompts/
│   ├── Baseline_prompt.py
│   ├── Detailed_prompt.py
│   └── Few_shot_prompt.py
│
├── Code/
│   ├── 1_Inference.py                   # API calls for receiver prediction
│   ├── 2_Turn_level_evaluation.py       # Turn-level evaluation metrics
│   ├── 3_Network_level_evaluation.py    # Network construction and analysis
│   ├── 4_Statistics.py                  # Statistics, self-assessed confidence scores, and logprob analysis
│   └── 5_Rem_analysis.py                # Relational event analysis
│
├── Data/
│   ├── Decoding/
│   │   ├── ID_debate_1.csv              # Mapping of speaker IDs to speaker names for Debate 1
│   │   ├── ID_debate_2.csv              # Mapping of speaker IDs to speaker names for Debate 2
│   │   ├── ID_debate_3.csv              # Mapping of speaker IDs to speaker names for Debate 3
│   │   ├── ID_debate_4.csv              # Mapping of speaker IDs to speaker names for Debate 4
│   │
│   └── Labeled_data/
│       ├── Debate_1.csv                 # Debate 1 with hand-annotated receivers (ground truth)
│       ├── Debate_2.csv                 # Debate 2 with hand-annotated receivers (ground truth)
│       ├── Debate_3.csv                 # Debate 3 with hand-annotated receivers (ground truth)
│       ├── Debate_4.csv                 # Debate 4 with hand-annotated receivers (ground truth)
│       ├── Last_speaker.csv             # Receiver predictions based on the last speaker
│       └── Recently_mentioned_participant.csv # Receiver predictions based on the recently mentioned participant
│
├── LICENSE.md
└── README.md
````

---

## Reproducing Results
Run code.
Run in numerical order.

## License
This project is released under the MIT License. See [LICENSE](LICENSE.md) for details.
