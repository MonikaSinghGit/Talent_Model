# Objective
- Using a dataset build a hiring system (predict “hire”, “rejected at interview”, or “rejected at pre-interview”)
- Deploying models that impact people requires careful ethical decision making.
- One of the components of ethical AI is Systematicity
- Arbitrariness: The inherent error in the model due to overfitting/underfitting or issues in the data (unpredictability, unconstrained, and unreasonable)
- Systematicity: A model (algorithm) with inherent arbitrariness used on a large scale within an entire sector (e.g. hiring, education, and loans) can produce systematic discrimination.
  - When deploying talent models at scale, we have to design systems that have some degree of randomness in order to ensure that individuals are not arbitrarily blocked from economic opportunities
  - Since we are unable to completely remove arbitrariness from a model, we may at least reduce its impact.
- The authors of the paper* outline two primary ways of addressing systematicity:
- Ensemble model method: Training a set of models (with similar accuracy) and randomly drawing from the set of models at prediction time (I chose to implement this one)
- Directly introducing (bounded) randomness to scores at prediction time

# Challenge
- A predict() function that implements one or more mechanisms for addressing systematicity
- A set of metrics and associated charts that allow someone to measure and evaluate the effectiveness of my systematicity mitigation strategy.

# Evaluation Metrics
The following are the two desirable behaviors of an ensemble technique addressing systematicity:
- Fairness: ensures that every deserving candidate is at least ‘hired’ once by an ensemble model.
- Arbitrariness: ensures that all deserving candidates have an equal chance of being “hired” by our ensemble model.






*Creel, Kathleen and Hellman, Deborah, The Algorithmic Leviathan: Arbitrariness, Fairness, and Opportunity in Algorithmic Decision Making Systems (February 15, 2021). Virginia Public Law and Legal Theory Research Paper No. 2021-13, Available at SSRN: https://ssrn.com/abstract=3786377

