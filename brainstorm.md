# Goal
The end goal of this project is to make an agent actually good at training machine learning models by applying RL techniques. 

We will need to design a robust evaluation suite, then create a well-defined RL environment to train our models on.

## What are LLMs bad at? 
* Designing comprehensive eval suites. A good eval framework is not just unit tests. It should be informative of errors/issues before they happen rather than having to inspect why something is wrong wrong.
* Diagnosing what actually went wrong. In ML settings, a number of things can go wrong when training, but LLMs often lose themselves in this space rather than really being able to investigate what is really going wrong.
* Pointing out issues when there is no _direct_ evidence pointing to an issue. LMs often tend to ignore potential issues of no evidence directly points to them, whereas a human may use their intuition to find these.
* Interpreting details like what a normal gap in train vs. validation/test metrics are compared to training numbers

## Our task
Given: 
1. A task for a model to complete, specifying inputs and expected outputs and behavior (whether in vision, language, multimodal, or other)
2. Hardware constraints
3. (Optional) model constraints

Train a machine learning model to reliably solve the task (or improve performance from a baseline).

## Evaluation
How do we measure success? What data? What metrics? 
1. Quality of final model (optionally compared to some baseline).
2. Compute/time/token spend
3. Quality of investigation and decisions (did each decision improve/degrade the model?)
