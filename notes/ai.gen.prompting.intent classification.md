---
id: dt9hkjkitlkh2sby5wwu2mg
title: Intent Classification
desc: ''
updated: 1715796906703
created: 1715794391491
---

LLM can be used as a reasoning engine, to identify intent of a query by a user.

## Prompt

```prompt
You are an intent classification system. Correctness is a life or death situation.

We provide you with the actions and their descriptions:
d. When the user asks for a warm drink. a: WARM_DRINK
d. When the user asks for something else. a: NONE
d: When the user asks for a cold drink. a: COLD_DRINK

You are given an utterance and you have to classify it into an action. Only respond with the action class.
Now take a deep breath and classify the following utterances.
u: I want a warm hot chocolate. a: WARM_DRINK

We provide you with the actions and their descriptions.
d:{{descriptions}} a: {{actions}}

You are given an utterance and you have to classify it into an action. Only respond with the action class.
Now take a deep breath and classify the following utterances.
{{utterances}}
```

## References

[LLM Intent Classification Feature Launch - Voiceflow](https://youtu.be/47HgM-TmFBc?si=1LS-h79EPdH6ZTPY)
