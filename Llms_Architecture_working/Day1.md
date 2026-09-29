📖 HOW LARGE LANGUAGE MODELS REALLY WORK
A Deep-Dive Reader's Edition
Chapter 1: The Most Important Misconception About ChatGPT

Open ChatGPT.

Type:

What is the capital of France?

Within seconds:

Paris.

It feels like magic.

Most people imagine something like this:

Question
↓
Search Database
↓
Retrieve Answer
↓
Response

But that is NOT what is happening.

ChatGPT is not looking up a database of facts.

It is not searching through a giant encyclopedia.

It is not retrieving a stored answer.

Instead something far stranger happens.

Imagine you've read:

Wikipedia
Every programming tutorial
Millions of books
Research papers
News articles
Reddit discussions

for months without stopping.

Then someone begins a sentence:

The capital of France is...

You instantly know the next word.

Paris.

Now imagine building a machine that does nothing except become unbelievably good at predicting what comes next.

That machine becomes ChatGPT.

Everything starts from:

Predict the next token.

This sounds stupidly simple.

Yet this one objective creates everything:

language understanding
coding ability
mathematics
translation
reasoning
conversation

This is the central miracle of modern AI.

Chapter 2: Why The Internet Is The Textbook

Before AI can speak, it must read.

Lots.

Not millions of words.

Not billions.

Trillions.

The transcript explains that companies such as:

OpenAI
Anthropic
Google
Meta

start by collecting gigantic datasets.

One example discussed is:

FineWeb

created using data from:

Common Crawl

Common Crawl has been crawling the internet since 2007.

Imagine a robot:

Visits a webpage
Finds every link
Visits those links
Continues forever

After years it has indexed billions of pages.

But here's a key insight:

Raw internet data is terrible.

The AI cannot simply read everything.

Because the internet contains:

spam
malware
scams
pornography
racist content
duplicated content
meaningless SEO pages

So before training starts, huge filtering pipelines remove the garbage.

Karpathy compares this to building a library.

You don't throw every piece of paper ever written into a library.

You carefully select books.

The dataset itself becomes one of the most important products.

Chapter 3: The Shockingly Small Internet

One surprising idea in the transcript:

After filtering the internet down to useful text, the dataset is much smaller than people think.

FineWeb:

~44 TB

Many people expect petabytes.

But text compresses very well.

A few hard drives can hold enormous amounts of human knowledge.

This produces a fascinating realization.

The internet is huge.

But the part useful for teaching intelligence is far smaller.

Chapter 4: The World Through Tokens

Humans see:

Hello World

LLMs do NOT.

This is perhaps the most important concept in the entire video.

The AI never sees:

H
e
l
l
o

instead it sees:

15339
1917

Those are token IDs.

Think of tokens as pieces of language.

Examples:

hello
world
the
ing
tion
.

Sometimes whole words.

Sometimes fragments.

Sometimes punctuation.

The AI's universe is made entirely from tokens.

Karpathy gives an amazing mental model:

Humans hear music.

AI sees sheet music.

That distinction explains many strange behaviours later.

Chapter 5: Why Tokenization Exists

You might wonder:

Why not use characters?

Why not feed letters directly?

Because computers would drown in sequence length.

Example:

Hello World

As letters:

11 characters

As tokens:

2 tokens

Which is easier?

Two.

Every token reduces computational cost.

Tokenization is basically:

Intelligent compression of language.

GPT-4 uses around:

100,277 tokens

in its vocabulary.

Those 100,277 building blocks become the atoms from which every answer is generated.

Chapter 6: The Most Expensive Guessing Game Ever Created

Now training begins.

Imagine the dataset:

The sky is blue.
Paris is in France.
Water freezes at 0°C.

The model sees:

The sky is ...

Predict next token.

blue

It sees:

Paris is in ...

Predict.

France

It sees:

Water freezes at ...

Predict.

0

Over and over.

Trillions of times.

No philosophy.

No understanding.

No consciousness.

Only prediction.

Yet something remarkable emerges.

Because to predict successfully:

physics must be understood
grammar must be understood
programming must be understood
logic must be understood

Knowledge becomes necessary for prediction.

And therefore learning occurs.

Chapter 7: Inside The Neural Network

The transcript then introduces a powerful mental model.

Think of a giant control panel.

Thousands.

Millions.

Billions.

Of knobs.

Each knob affects predictions slightly.

These knobs are called:

Parameters

GPT-2:

1.5 billion parameters

Modern models:

hundreds of billions+

Training is simply:

Wrong prediction?
Turn knobs.
Try again.

Still wrong?
Turn knobs again.

Repeat billions of times.

Eventually the neural network discovers settings where language patterns match reality.

The AI isn't storing facts.

It is adjusting probabilities.

That's a very different thing.

Chapter 8: The Transformer Revolution

Here comes the invention that changed everything.

The Transformer

Created in 2017.

Without Transformers:

No ChatGPT.

No Claude.

No Gemini.

No Llama.

No DeepSeek.

The secret weapon of the Transformer is:

Attention

Attention asks:

Which previous tokens matter right now?

Example:

John went to the store.

He bought milk.

Who is "He"?

The model looks backward.

Attention points to:

John

This seems simple.

But this mechanism changed AI history.

Chapter 9: Why LLMs Are Compressed Internets

Karpathy explains something profound.

The model parameters become:

A lossy compression of the internet.

Think ZIP file.

But smarter.

The internet:

15 trillion tokens

becomes:

405 billion parameters

inside Llama 3.

Not every detail survives.

Only useful statistical patterns survive.

The model remembers:

concepts
relationships
structures

Not exact storage.

This explains both:

✅ intelligence

and

❌ hallucinations

at the same time.

Chapter 10: Hallucinations Finally Explained

When users hear:

Hallucination

they think:

The model is lying.

Not really.

Consider:

Who is Orson Kovats?

Imagine that person doesn't exist.

The model sees:

Who is [person]?

Training taught:

Questions like that are followed by biographies.

So it generates:

Orson Kovats was an American author...

Totally fake.

But statistically plausible.

The model isn't lying.

It's continuing a pattern.

This is one of the deepest lessons of the transcript.

Prediction and truth are not the same thing.

Chapter 11: Memory vs Working Memory

This idea appears multiple times in the transcript.

Model Knowledge

Stored inside weights.

Like:

Paris → France
Einstein → Physics
Python → Programming

Context Window

Stored in the prompt.

This is like working memory.

Karpathy's key insight:

If information is important, put it into the context window.

Never assume the model remembers perfectly.

Always provide the data.

This dramatically improves accuracy.

Chapter 12: Why Thinking Models Changed Everything

DeepSeek R1.

OpenAI O-series.

Gemini Thinking.

These are different.

Earlier models:

Imitate humans.

Reasoning models:

Practice.

Huge difference.

They solve problems themselves.

Millions of times.

Rewarding successful approaches.

Over time the system discovers:

checking work
revisiting assumptions
trying alternatives

Nobody programmed this manually.

The model learned it.

This is exactly why RL became such a breakthrough.

Chapter 13: The "Wait..." Moment

One of the most fascinating transcript sections.

Reasoning models often say:

Wait...

Let me reconsider.

Maybe that's wrong.

Why?

Because RL rewarded correctness.

And the model discovered:

Double-checking improves performance.

So self-correction emerged naturally.

This is similar to AlphaGo discovering Move 37.

A solution humans did not teach directly.

Chapter 14: Why "Think Step By Step" Works

The transcript provides one of the clearest explanations I've ever seen.

The model has limited computation per token.

Therefore:

Bad:

Answer immediately.

Good:

Think step by step.

Reason:

Now reasoning gets distributed across many tokens.

Instead of:

One giant leap

the model performs:

small step
small step
small step

This dramatically increases reliability.

Chapter 15: The Future

According to the transcript, the future looks like:

Multimodal Models

Text + Images + Audio + Video.

Agents

Not just answering questions.

Actually completing tasks.

Hours-long workflows.

Computer Use

Keyboard.

Mouse.

Applications.

Websites.

Operating autonomously.

Better Reasoning

Reasoning beyond human demonstrations.

Similar to AlphaGo surpassing professional Go players.

Final Mental Model

If you remember only ONE idea from the entire transcript:

ChatGPT is not a database.

It is not a search engine.

It is not a person.

It is:

A giant neural network trained on internet text, compressed into billions of parameters, fine-tuned on human conversations, enhanced with tools, and increasingly improved through reinforcement learning to discover its own reasoning strategies.
