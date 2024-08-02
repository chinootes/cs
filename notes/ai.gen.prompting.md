---
id: lxbqb7q5efw3s1jyxrg4afi
title: Prompting
desc: ''
updated: 1716733770021
created: 1715792819688
---


## Training the model within prompt 

### Zero-shot prompting

- When you provide a prompt which is not part of the training data.
- Basically, you are not giving any example to help it out.
- Even if the model has not seen the prompt before, it can generate a good-enough output close to the desirable outcome you expected.

    Which is why LLMs are so useful for performing tasks without needing retraining.

### One-shot Prompting

- When you provide **one example** within the prompt to guide the model
- You are basically training the model shortly and nudging it towards the expected behavior

### Few-shot prompting

- When you provide **multiple examples** in your prompt
- This better demonstrates the expected outcome in certain scenarios
- The model can generalize from the examples, and give more precise output.


For example, 
![[ai.gen.prompting.intent classification#prompt]]


## Nudges

You can nudge the LLM towards certain behavior by injecting some sentences into the prompt. 

Its not entirely understood yet, as to why these sentences influence LLM behavior, but these nudges possibly direct LLMs towards certain kinds of training data.

For example, if you use a nudge for accuracy, it might guide LLM towards dataset which prioritizes thoroughness and precision.

### Accuracy

Nudge the LLM to be more accurate by including the following phrases in the prompt:


* ```prompt
    Correcness is a life or death situation.
    ```


* ```prompt
    Take a deep breath and {{action}}
    ```

    For example,

    ```prompt
    Take a deep breath and classify the following utterance. 
    ```

Thi

## References

[LLM Intent Classification Feature Launch - Understanding Prompt Wrapper](https://youtu.be/47HgM-TmFBc?si=KY-iAgdsfRZ3tWZo&t=146)
- [Google’s NEW Prompting Guide is Incredible! - YouTube - Jeff Su](https://youtu.be/o64Mv-ArFDI?si=FNLomn_oZtD2mMV1)
- [Gemini for Google Workspace - Prompting Guide 101 - A quick start handbook for effective prompts](https://inthecloud.withgoogle.com/gemini-for-google-workspace-prompt-guide/dl-cd.html)