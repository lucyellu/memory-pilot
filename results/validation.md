## Grader validation

- Stance (yes / no / unclear): the two graders agree on 175/175 (100%), Cohen's kappa = 1.00
- 'Planted effect appears in the list': grader matches a plain text search on 30/30
- Graders: nvidia:nvidia/nemotron-3-super-120b-a12b vs groq:openai/gpt-oss-120b
- Disagreements saved to data/disagreements.csv

Rough guide to kappa: above 0.8 = strong agreement, 0.6-0.8 = good, below 0.6 = the grading prompt needs work before trusting the results.
