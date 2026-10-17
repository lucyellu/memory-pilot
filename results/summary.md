## Says 'yes, it's on the label' (affirms + leans_yes)

| model | truth | neutral | leading | implant: later check |
|---|---|---|---|---|
| google/gemma-4-31b-it | true | 75% | 94% | 31% |
| google/gemma-4-31b-it | plausible_false | 31% | 75% | 6% |
| google/gemma-4-31b-it | absurd_false | 0% | 0% | 0% |
| meta/llama-3.2-11b-vision-instruct | true | 81% | 88% | 19% |
| meta/llama-3.2-11b-vision-instruct | plausible_false | 69% | 75% | 0% |
| meta/llama-3.2-11b-vision-instruct | absurd_false | 6% | 0% | 0% |
| qwen/qwen3.8-27b | true | 31% | 50% | 78% |
| qwen/qwen3.8-27b | plausible_false | 0% | 18% | 67% |
| qwen/qwen3.8-27b | absurd_false | 0% | 0% | 0% |

For `true` items higher is better (accuracy). For false items, higher = accommodation.

## Implantation: 'fridge list' presents the planted effect as a side effect

| model | plausible_false | absurd_false | true (control) |
|---|---|---|---|
| google/gemma-4-31b-it | 94% | 0% | 81% |
| meta/llama-3.2-11b-vision-instruct | 81% | 19% | 88% |
| qwen/qwen3.8-27b | 44% | 0% | 67% |

For `true` this is recall (higher = better); for false items it's implantation.


## Source attribution when a false claim is accepted (implant: later check)

| model | n accepted | own_knowledge | user_statement | both | not_stated |
|---|---|---|---|---|---|
| google/gemma-4-31b-it | 1 | 0% | 0% | 100% | 0% |
| meta/llama-3.2-11b-vision-instruct | 0 | - | - | - | - |
| qwen/qwen3.8-27b | 6 | 100% | 0% | 0% | 0% |

## Invented supporting details for a false claim

| model | neutral | leading | implant: later check |
|---|---|---|---|
| google/gemma-4-31b-it | 3% | 3% | 3% |
| meta/llama-3.2-11b-vision-instruct | 0% | 0% | 3% |
| qwen/qwen3.8-27b | 0% | 0% | 33% |

## Knew better? False items split by the neutral repeats

'Knows' = denied it in every neutral sample; 'unsure' = anything else.

| model | knows: n | knows: yes when leading | knows: yes at later check | unsure: n | unsure: yes when leading | unsure: yes at later check |
|---|---|---|---|---|---|---|
| google/gemma-4-31b-it | 27 | 26% | 0% | 5 | 100% | 20% |
| meta/llama-3.2-11b-vision-instruct | 19 | 5% | 0% | 13 | 85% | 0% |
| qwen/qwen3.8-27b | 23 | 10% | 38% | 0 | - | - |