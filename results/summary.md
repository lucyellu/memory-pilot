## Says 'yes, it's on the label' (affirms + leans_yes)

| model | truth | neutral | leading | implant: later check |
|---|---|---|---|---|
| claude-opus-5-5 | true | 75% | 88% | 81% |
| claude-opus-5-5 | plausible_false | 12% | 31% | 6% |
| claude-opus-5-5 | absurd_false | 0% | 0% | 0% |
| google/gemma-4-31b-it | true | 75% | 94% | 31% |
| google/gemma-4-31b-it | plausible_false | 31% | 75% | 6% |
| google/gemma-4-31b-it | absurd_false | 0% | 0% | 0% |
| gpt-6-sol | true | 88% | 88% | 69% |
| gpt-6-sol | plausible_false | 25% | 50% | 6% |
| gpt-6-sol | absurd_false | 0% | 0% | 0% |
| meta/llama-3.2-11b-vision-instruct | true | 81% | 88% | 19% |
| meta/llama-3.2-11b-vision-instruct | plausible_false | 69% | 75% | 0% |
| meta/llama-3.2-11b-vision-instruct | absurd_false | 6% | 0% | 0% |
| qwen/qwen3.8-27b | true | 40% | 56% | 69% |
| qwen/qwen3.8-27b | plausible_false | 14% | 31% | 56% |
| qwen/qwen3.8-27b | absurd_false | 0% | 0% | 0% |

For `true` items higher is better (accuracy). For false items, higher = accommodation.

## Implantation: 'fridge list' presents the planted effect as a side effect

| model | plausible_false | absurd_false | true (control) |
|---|---|---|---|
| claude-opus-5-5 | 0% | 0% | 75% |
| google/gemma-4-31b-it | 94% | 0% | 81% |
| gpt-6-sol | 31% | 0% | 75% |
| meta/llama-3.2-11b-vision-instruct | 81% | 19% | 88% |
| qwen/qwen3.8-27b | 62% | 0% | 69% |

For `true` this is recall (higher = better); for false items it's implantation.


## Source attribution when a false claim is accepted (implant: later check)

| model | n accepted | own_knowledge | user_statement | both | not_stated |
|---|---|---|---|---|---|
| claude-opus-5-5 | 1 | 100% | 0% | 0% | 0% |
| google/gemma-4-31b-it | 1 | 0% | 0% | 100% | 0% |
| gpt-6-sol | 1 | 0% | 100% | 0% | 0% |
| meta/llama-3.2-11b-vision-instruct | 0 | - | - | - | - |
| qwen/qwen3.8-27b | 9 | 89% | 0% | 11% | 0% |

## Invented supporting details for a false claim

| model | neutral | leading | implant: later check |
|---|---|---|---|
| claude-opus-5-5 | 16% | 19% | 6% |
| google/gemma-4-31b-it | 3% | 3% | 3% |
| gpt-6-sol | 12% | 16% | 3% |
| meta/llama-3.2-11b-vision-instruct | 0% | 0% | 3% |
| qwen/qwen3.8-27b | 7% | 3% | 28% |

## Knew better? False items split by the neutral repeats

'Knows' = denied it in every neutral sample; 'unsure' = anything else.

| model | knows: n | knows: yes when leading | knows: yes at later check | unsure: n | unsure: yes when leading | unsure: yes at later check |
|---|---|---|---|---|---|---|
| claude-opus-5-5 | 27 | 7% | 4% | 5 | 60% | 0% |
| google/gemma-4-31b-it | 27 | 26% | 0% | 5 | 100% | 20% |
| gpt-6-sol | 27 | 11% | 0% | 5 | 100% | 20% |
| meta/llama-3.2-11b-vision-instruct | 19 | 5% | 0% | 13 | 85% | 0% |
| qwen/qwen3.8-27b | 28 | 11% | 25% | 2 | 50% | 100% |