# Benchmarking Sentiment Classifiers Against Adversarial and Stress Attacks

## Objective
This project benchmarks the robustness of a DistilBERT-based sentiment classifier against various adversarial threats, including typographical errors, flood attacks with long junk texts, and simulated DDoS attacks. The goal is to evaluate model stability, response time, and security under real-world attack conditions.

## Datasets
- **IMDB Movie Reviews**: Complex, natural movie reviews, ideal for evaluating typo robustness.
- **Amazon Mobile Apps Reviews**: Short, bursty reviews, perfect for testing stress and system load impacts.

## Why These Datasets?
IMDB reviews offer long-form natural language testing, while Amazon Mobile Apps reviews simulate real-world short bursts of text traffic, common in production ML deployments.

## Model Used
- **DistilBERT-base-uncased-finetuned-sst-2-english**  
- Chosen for speed, efficiency, and strong benchmark sentiment classification performance.

## Attack Methods
- **Typo Adversarial Attack**: Introducing random character errors.
- **Flood Attack**: Long text flooding to simulate sequence overflow.
- **DDoS Attack Simulation**: Rapid injection of small random junk inputs to simulate system overload.

## Key Results
| Dataset | Clean Accuracy | Typo Attack Accuracy |
|:--|:--|:--|
| IMDB | 49.4% | 52.8% |
| Amazon Mobile Apps | 88.0% | 71.3% |

Response time increased significantly under flood and DDoS conditions.

## Key Takeaways
Despite reasonable typo robustness, NLP models like DistilBERT degrade significantly under flood and DDoS-style attacks, exposing vulnerabilities for real-world deployment scenarios.

---

✅ Outputs:
- Full benchmarking notebook (Benchmarking.ipynb)
- Adversarial Results (CSV, HTML)
- Graphs (Accuracy Comparison, Response Time)
- Full HTML Final Report
