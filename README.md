# EleutherAI Info

An unofficial hub for onboarding & other information.

## Quick Info

### Announcements

🔔🔔 *[This Announcement Does Not Exist](https://github.com/EleutherAI/info/blob/main/ANNOUNCEMENTS.md)* (Feb. 30) 🔔🔔

### Project Statuses
(*Last updated October 29, 2020*)
* __GPT-Neo__: Architecture built. 1.3B model trained. Release pending evaluations.
* __Pile™ v1__: Data collected. Deduplication in progress. Release pending writeup.
* __Pile™ v2__: Data collection begun. Looking for > 10GiB datasets, non-English.
* __Radioactive Lab__: Experiments begun. Reworking after [feedback from authors](https://github.com/facebookresearch/radioactive_data/issues/3).

### Links
* [Download the data](https://github.com/EleutherAI/The-Pile)
* [Check out the model code](https://github.com/EleutherAI/GPTNeo)
* [Watch the models train](https://kevinwatkins.github.io/foomboard/)


## About

EleutherAI (/iˈluθər eɪ. aɪ/) is a grassroots collection of researchers with a common goal of open sourcing language models. Founded in July of 2020, our flagship project is GPT-Neo, a replication of OpenAI's massive 175B parameter language model, GPT-3.

### Projects

#### [GPT-Neo](https://github.com/EleutherAI/GPTNeo)

GPT-Neo is the code name for a series of transformer-based language models loosely styled around the GPT architecture that we plan to train and open source. Our primary goal is to replicate a GPT-3 sized model and open source it to the public, for free. 

Along the way we will be running experiments with alternative architectures and attention types, releasing any intermediate models, and writing up any findings on our blog. 

Our models are built in [Mesh TensorFlow](https://github.com/tensorflow/mesh), which will allow us to scale up to GPT-3 sizes and beyond using simultaneous model and data parallelism. 

#### [The Pile™](https://github.com/EleutherAI/The-Pile)

The Pile is a large, diverse, open source language modelling data set that consists of many smaller datasets combined together. The objective is to obtain text from as many modalities as possible to ensure that models trained using The Pile will have much broader generalization abilities. We are currently developing Version 1, with a goal of [1 TiB of English text](https://github.com/EleutherAI/The-Pile). After the completion of Version 1, our next goal is a [fully-multilingual, 10TiB text dataset](https://github.com/EleutherAI/The-Pile/tree/version2).

#### [The Radioactive Lab](https://github.com/EleutherAI/radioactive-lab)

Modern deep learning systems are commonly deployed in distributed and cloud settings, which raises a fundamental question of trust: if a model is executed by a third party, how can the model owner know that it was executed correctly? A cloud server that cuts corners could implement a simpler model to save compute costs, and a malicious cloud server could actively seek to mislead the model owner about it's outputs. These questions also are important in the context of public trust in AI: can an organization that is untrusted by the public in some way prove that their models are working as advertised?

Other closely related questions relate to ownership of models and data. Model stealing and data stealing attacks have the ability to compromise individual and company privacy and intellectual property. This application is particularly important to EleutherAI as an organization that distributes open-source software. We are proud to offer all of our work open source, but we would like to know who is using our models and for what purposes.

### Other Activities

* __HUMONGOUS__: In order to feed growing multilingual language models, we'd like to build on the massive amount of webpages that [Common Crawl](https://commoncrawl.org/) has archived. HUMONGOUS is our attempt to convert *all* of the Common Crawl dumps---more than a petabyte of data---into useable, LM-ready text.
* __Alignment Reading Group__: Many of us believe that [aligning artificial intelligences](https://www.youtube.com/watch?v=EUjc1WuyPT8&t=431s) is potentially _the most pressing issue_ for us to address, long term. 
* __Interpretability__: Understanding what language models (LMs) are doing and why is of interest to many members of the NLP community. One of our channels is dedicated to just this kind of work.
* __Research__: Chatting about whatever research is of interest, be it group theory, scaling laws, neuromorphic computing, or anything else under the sun.


## Q&A

### General

Q: *How did this all start?*

A: something something . . . Connor Leahy . . . something something

Q: *How can I get involved?*

A: Join our [Discord](https://www.google.com/url?q=https%3A%2F%2Fdiscord.gg%2FMjSbyKa&sa=D&sntz=1&usg=AFQjCNHLFs5N2ipCqFsV9tnQvcAJ26BSxg) or check out our [Github](https://github.com/EleutherAI)! We're an open community, so you are free to contribute as you wish. We welcome contributors of all backgrounds and experience levels: there's lots to do. Since you're reading this, you've already found our information repo, which should be enough to get you up to speed on our work.

Q: *Are there any other ways to support EleutherAI?*

A: Our biggest needs at the moment in the __compute__ department. If you or someone you know has access to large quantities of CPU, GPU, or TPU resources, send a message to Sid with more details.

Q: *So . . . what's the deal with your logo?*

A: In keeping with the theme, our logo and font are also AI-generated.

Q: *Where can I go if I have more questions?*

A: The Discord is the best place for that. The community has always been helpful to new, curious members. Additionally, some of our core contributors' usernames will appear in purple or green in the chat.

### GPT-Neo

Q: *How are you going to train such a big model?*

A: We have built a [framework](https://github.com/EleutherAI/GPTNeo) using Mesh Tensorflow that lets us train models at super-large scales, including on GPUs and TPUs. At the moment, we have limited access to preemptible TPUs through the [TensorFlow Research Cloud (TFRC) program](https://www.tensorflow.org/tfrc). In the future, our plan is to ask "*please, sir, may I have some more?*". In the event such a plan does not work, we will consider other options.

Q: *What about distributed computing, like [Folding@Home](https://foldingathome.org/) or [hivemind](https://github.com/learning-at-home/hivemind)?*

A: We've considered the possibility of pooling GPUs for training models. In short, doing it well, and at this scale is an unsolved problem that would take a lot of work to make happen. If you have expertise in this area, though, folks would be happy to hear you out.

Q: *How big is the largest model you've trained?*

A: At the time of writing---October 27th, 2020---we've trained many models under many configurations. The largest we have trained at all clocked in at 100B parameters. For full training, our largest yet is 1.3B parameters, approximately the same size as GPT-2 XL, and used OpenWebText as its corpus. In the near future, we will be training a set of smaller models on The Pile™ and Common Crawl.

Q: *How's the model doing?*

A: Well! (I think) If you're curious about how our models are doing, you can watch them train on the lovely [Foomboard](https://kevinwatkins.github.io/foomboard/).

Q: *Have you considered more efficient architectures?*

A: Yes, we are exploring the full design space, including various linear-scaling attention mechanisms. In general, we have found that a mix of global and local attention is important for robust performance.


Q: *Is GPT-Neo free software?*

A: We have not determined the licensing situation of GPT-Neo yet. It's possible we might use some combination of permissive licensing for the code and copyleft licensing for the models themselves. We'll see.

### The Pile™

Q: *What's in the Pile™?*

A: The Pile™ is a collection of many smaller datasets. It includes a large diversity of text, from academic writing, to legal texts, to online literature, video subtitles, and more. This abundance means that saying precisely what is in this meta-dataset is difficult. If you are interested in exploring this, send a message to `#the-pile` on Discord.

Q: *What's the format of the Pile™?*

A: We use a simple, compressed JSON format of our own design called [lm_dataformat (LMD)](https://github.com/leogao2/lm_dataformat). It's designed to make writing, storing, and reading text simple and performant. Every logical document maps to a JSON object with `text` and `meta` fields, and batches of these objects are compressed using `zstd` or `gz`.

Q: *Who can use the Pile™?*

A: The Pile™ was primarily designed for researchers training large-scale langauge models. It also may be of interest to other researchers interested in topics such as bias, online discourse, and text compression.

Q: *Is the Pile™ released yet?*

A: No.

Q: *When will the Pile™ be released?*

A: Soon . . .

Q: *Where will I be able to get the Pile™ once it's released?*

A: We are looking to potentially announce several options for folks to source the Pile™ from. Be on the lookout for announcements.

Q: *Can I add something to the Pile™?*

A: Yes! The process for adding a new dataset to the collection is outlined in the [repo](https://github.com/EleutherAI/The-Pile). All contributions intended for v2 will go to the `version2` branch.

Q: *Can I make my own version of the Pile™?*

A: Of course! For just this reason, all of the components are reproducible. Look for a repo labeled as `pile-[COMPONENT]` or `pile_[COMPONENT]` if you want to reproduce a component. We also may provide links to pre-processed components to allow you to mix, match, and re-sample to derive your own datasets.

### The Radioactive Lab

Q: *How do you plan on making your models "radioactive"?*

A: The Rad Lab is pursuing a number of directions to stamp our models. One of particular interest is through the use of "radioactive data", which was an approach introduced by [this paper](https://arxiv.org/abs/2002.00937).

### Other Activities

#### HUMONGOUS

Q: *Why are you building HUMONGOUS?*

A: Because none of the other Common Crawl-extracted datasets met our needs. For Pile™ v2, we will need tens of terabytes of clean, multilingual text, which is quite hard to come by! For that, we felt that building our own pipeline to extract LM-ready text from raw WARC (Web ARChive) files was the best strategy.


Q: *How is HUMONGOUS different from ([OSCAR](https://oscar-corpus.com/)/[C4](https://www.tensorflow.org/datasets/catalog/c4)/[CC100](http://data.statmt.org/cc-100/))?*

A: Compared to other Common-Crawl derived datasets, HUMONGOUS aims to do a couple of things:
* Start from the raw WARC files, rather than WET files, which allows us to extract better text.
* Be fully multi-lingual, covering as many languages as we can identify.
* Process all Common Crawl dumps, past and future, not just one month's snapshot.