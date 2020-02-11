![](https://raw.githubusercontent.com/ricsonc/parameter-count-trend/master/params.png)

OpenAI has [their analysis on compute power over time](https://openai.com/blog/ai-and-compute/), so I'd figure I'd plot number of model parameters over time. This should be interesting in the sense that # parameters is a loose proxy for the expressive power of a model. The human brain is estimated to have 100 trillion synapses, so assuming a one-to-one correspondence between synapses and parameters, we're only 3-4 orders of magnitude off. 

I selected a few dozen influential and "memorable" papers from the decade or so -- basically just papers off the top of my head. Apologies if I omitted your favorite model. I tried to go for some amount of diversity. Models are colored by area -- Green: language models, Blue: general CNN backbones, Purple: applied computer vision, Magenta: generative image models, Turqoise: misc, Red: reinforcement learning.

I tried to find the number of parameters if it was written in the paper. If multiple models were specified in a paper, I took the largest one. In some cases, I manually computed a rough estimate of the number of parameters. I did my best, but no guarantees of correctness on my estimates. Sometimes I was able to find parameter count information in survey papers. I excluded models like sparse MoE (138B params), SNM5 (33B), and BigLSTM (3.3B) because I felt that their "parameters" didn't follow the spirit of the inquiry here -- for a typical input, the vast majority of paramters are not used in the computation of the output. Of course the boundary is very fuzzy. 

Observations:

1. Language models have always been about an order of magnitude larger than vision models, and vision an order of magnitude larger than RL.
2. One could draw a nice trend-line from Inception-v3 to T-NLG and say that #parameters doubles every 5 months. Of course this is probably spurious.
3. Parameter count hasn't grown as dramatically as compute power. sub-1B parameter models can usually fit on 1 GPU without too much trouble.
4. Popular backbone networks and "applied" computer vision models haven't really grown in size at all. 

