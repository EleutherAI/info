## Research Ideas

This document is for tracking research ideas that are appealing but nobody is actively working on. If any of these sound cool to you, bring it up in #research. Often times these ideas have people interested in them, but nobody is pushing for it enough to motivate people to work on it. If you think that that can be you, claim it!

### Data

### Language Modeling

#### Transformers on formal languages

#### Level set estimation for transformers

**Point of Contact:**
* Stella Biderman

### Scaling Laws

### Reinforcement Learning

#### Partial preference learning

There’s at type of RL that’s known as “inverse reinforcement learning” or “learning from demonstrations” because it’s basically the reverse of normal RL. You don’t have access to the reward function but instead you have access to policies created by experts. The goal is the same: you want to learn successful policies. One very interesting aspect of this is that getting superhuman performance is very hard.

A recently paper ([paper](http://proceedings.mlr.press/v119/reddy20a/reddy20a.pdf), [code](https://github.com/rddy/ReQueST)) did an interesting variant of this where they used active learning. The AI generated potential routes and then had an oracle it could query to ask if they were good and sought to simultaneously maximize reward and minimize the number of queries.

I think that there’s a nice extension that’s more realistic end more useful. They had you query an entire route and the queries had constant cost. I want to make the AI query partial paths and have the cost dependent on the length of the policy. I did some math and have reason to believe that this will lead to interesting behavior.

Another cool aspect of this project is that it has alignment implications. This is discussed a bit in the linked paper, but IRL and preference learning are very nearly the same thing with different wording. Anything we develop that improved an RL agent’s ability to navigate a maze will also be able to be used to help an RL agent learn human morality.

**Point of Contact:**
* Stella Biderman

### ML Theory
