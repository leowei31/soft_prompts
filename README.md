# Objectives

The goal of this project is to build soft prompt enabled agents. Proof of concept of soft prompts for SLMs, and verify soft prompt effectiveness compared to traditional zero shot hard prompting.

In this repo, I've also included my own research where I use soft prompts for anomly detection in time series data. The paper won best paper award at a IEEE conference.

## Drawbacks to soft prompts

I wondered about this a lot this past week on why soft prompts are not more popular, why not everybody is using them. I was able to deduce a few reasons myself.

* Lack of open sourced models: training soft prompts requires gradients updates, with all these SOTA models behind APIs, it's hard to train soft prompts. And on top of that, training soft prompts for these extremely large models is going to take forever.
* Black box nature: soft prompts are just trainable embeddings treated like a black box, hard to see what they are actually doing. Meanwhile compared to hard prompting, you can see exactly what the prompt is and what the system user is asking the LLM to do.
* Not very future proof if you want to use SOTA models: since soft prompts are model dependent, and the pace of models that are coming out is so fast, optimizing soft prompts are model specific, so this gets hard because nowadays a new models comes out like every week, would be nice if soft prompts can be better initialized with transfer learning or something though.
* Cost to benefit ratio: I bet hard prompting is probably way cheaper than training soft prompts even if you are optimizing your hard prompts manually. Soft prompting requires hyperparameter selection, training the soft prompt meaning you have to host the model yourself, which is not cheap if you want something more than just a couple b params.
