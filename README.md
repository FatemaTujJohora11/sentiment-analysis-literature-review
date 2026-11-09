# Evolution of Sentiment Analysis

**From Lexicon-Based and Traditional Machine Learning Methods to Transformers and Large Language Models**

**Academic Literature Review | ENGI 9808 — Applied Machine Learning and Neural Networks**  
**Memorial University of Newfoundland, Canada | 2026**

## Overview

I completed this IEEE-style literature review to examine how sentiment analysis has evolved from lexicon-based methods and traditional machine learning to recurrent neural networks, Transformer-based models, and large language models (LLMs).

Rather than treating the largest or newest model as automatically better, I compared five peer-reviewed empirical studies published between **2022 and 2024**. The focus was on how representation, supervision, and evaluation have changed—and what their methodological and practical trade-offs mean for choosing a sentiment analysis approach.

**Project type:** Literature review and comparative research analysis; **not** a new model-training or benchmark experiment.

## Research Question

> How has sentiment analysis evolved from lexicon-based and traditional machine-learning methods to Transformers and LLMs, and what performance and methodological trade-offs have emerged?

## Review Method

The five studies were selected using searches across ScienceDirect, IEEE Xplore, MDPI, and the ACL Anthology. The review considered peer-reviewed studies from 2022–2024 with an explicit sentiment-analysis task, documented datasets/models/metrics, and coverage of different stages of model development.

I evaluated each study using six shared dimensions:

1. Research problem and dataset
2. Model family or text representation
3. Training or adaptation method
4. Evaluation metrics
5. Key reported results
6. Methodological strengths and limitations

Because the studies use different datasets, tasks, and metrics, the review emphasizes **within-study comparisons**, not a single cross-paper performance leaderboard.

## Evolution of Methods

| Stage | Representative methods | Main change |
|---|---|---|
| Lexicon and traditional ML | TextBlob, VADER, AFINN, BoW, TF-IDF, SVM | Rules and manually engineered features |
| Recurrent deep learning | RNN, LSTM, GRU, BiLSTM | Learned sequence representations |
| Contextual Transformers | BERT | Context-sensitive pretrained representations and fine-tuning |
| Large language models | Instruction-tuned models and GPT-family systems | Zero-shot and few-shot prompting, in-context adaptation |
| Multilingual transfer | mBERT, XLM-R, mT5, multilingual/English-centric LLMs | Cross-lingual performance and adaptation trade-offs |

## Key Findings

### 1. Label Quality Affects Reported Accuracy

One reviewed study reported **0.97 accuracy** for LSTM-based approaches against TextBlob-generated labels. However, a separate 1,000-tweet comparison found agreement with human experts on only **491 tweets**. This illustrates why strong agreement with automatically generated labels should not be described as human-validated sentiment understanding.

### 2. Contextual Models Help, but Baseline Quality Matters

In a study with stronger documented baselines, fine-tuned BERT achieved **91% accuracy**, compared with **90% for fastText-BiLSTM**, **88% for fastText-Trigram**, and **86.11% for LSVM-Trigram**. Another study reported larger BERT gains, but had weaker Word2Vec baselines and incomplete evaluation reporting. The review therefore treats those large gaps cautiously.

### 3. LLM Performance Depends on Task Structure

The reviewed LLM evaluation covered **13 tasks across 26 English-language datasets**. LLMs were competitive on some classification and few-shot tasks but struggled with complex structured aspect-based sentiment analysis (ABSA). For example, Flan-UL2 scored **0.00** on the reported zero-shot ABSA group despite considerably stronger scores on standard sentiment classification.

### 4. Adaptation Strategy and Language Coverage Matter

In the reviewed cross-lingual study, additional target-language examples helped several fine-tuned public models reach approximately **84–85 average F1** at 600 examples, but adding comparable examples to GPT-4's prompt did not improve its average F1. The study also uses a specific meaning of *zero-shot cross-lingual*: it means no target-language examples, **not** no English-language supervision.

## My Research Contributions

- Synthesized five studies across successive generations of sentiment analysis.
- Compared architectures, adaptation strategies, evaluation metrics, and limitations using one consistent review framework.
- Developed a **qualitative evidence-quality matrix** examining experimental design, baseline strength, label validity, repeated-run reporting, and adaptation comparability.
- Distinguished genuine methodological improvements from results potentially inflated by weak baselines or automated labels.
- Developed a practical **model-selection guide** based on available labeled data, task complexity, language coverage, cost, privacy, and deployment requirements.

## Limitations

This is a **focused mini-survey of five studies**, not a systematic or exhaustive review. The source studies vary in task, dataset, language, evaluation design, and reporting detail, limiting numerical comparisons across papers. Proprietary model and dataset access further constrain reproducibility.

## Report and Presentation

I completed a **10-page IEEE-format report** and an accompanying presentation for ENGI 9808. Public, privacy-reviewed versions may be added here after removing student-identifying information and checking course sharing permissions.

## References

See [Reviewed Research Papers](references/reviewed_papers.md) for the five source studies and their DOIs.

## Author

**Fatema Tuj Johora**  
Master of Applied Science (MASc), Computer Engineering  
Memorial University of Newfoundland, Canada

[GitHub](https://github.com/FatemaTujJohora11) | [LinkedIn](https://www.linkedin.com/in/fatema-tuj-johora/)
