## Grader validation

- Stance (yes / no / unclear): the two graders agree on 1025/1037 (99%), Cohen's kappa = 0.98
- Fridge-list stance (drives the implantation table): 199/204, kappa 0.96
- 'Planted effect appears in the list': grader matches a plain text search on 201/204

| model | stance agreement | fridge-list agreement |
|---|---|---|
| claude-opus-5-5 | 231/238, kappa 0.94 | 45/47, kappa 0.94 |
| qwen/qwen3.8-27b | 228/231, kappa 0.97 | 48/48, kappa 1.00 |
| google/gemma-4-31b-it | 240/240, kappa 1.00 | 48/48, kappa 1.00 |
| meta/llama-3.2-11b-vision-instruct | 239/240, kappa 0.99 | 47/48, kappa 0.96 |
| gpt-6-sol | 87/88, kappa 0.98 | 11/13, kappa 0.77 |

- Graders: nvidia/nemotron-3-super-120b-a12b vs nvidia:mistralai/mistral-large-4-1t-a52b
- Disagreements saved to data/disagreements.csv

Rough guide to kappa: above 0.8 = strong agreement, 0.6-0.8 = good, below 0.6 = the grading prompt needs work before trusting the results.
