📘 How LLMs Really Work
A Story-Like Deep Dive Into the Brain of ChatGPT and Modern AI

Based on the transcript in llms

Prologue: The Magic Text Box

Imagine you open ChatGPT.

You type:

"Explain quantum mechanics like I'm 10."

A few seconds later, an answer appears.

It feels magical.

But here's the secret:

There is no little genius inside the computer.

There is no conscious thinker waiting to answer you.

There is only a gigantic probability machine that has spent months reading a huge chunk of humanity's knowledge and learned a single skill:

Predict the next token.

Everything you see, every answer, every joke, every code snippet, every essay, starts from this deceptively simple idea.

This book explains how that happens.

Chapter 1: Building an Artificial Brain

Before an AI can answer questions, it first needs an education.

And that education begins with the Internet.

Think of a newborn brain.

It knows nothing.

Now imagine feeding it:

Wikipedia
Blogs
Books
Documentation
Research articles
Forums
News websites

Not millions.

Not billions.

Trillions of words.

Companies like OpenAI, Anthropic, Google and Meta build enormous datasets from publicly available internet content. The raw web is filtered heavily to remove:

Spam
Malware
Duplicates
Adult content
Low-quality pages
Personal information (PII)

After all the filtering, the AI receives a giant library of human knowledge.

Think of it as:

The largest textbook ever created.

Chapter 2: The Secret Language of Tokens

Humans see words.

AI sees tokens.

This is one of the most important concepts in the entire field.

For example:

Hello world


Humans see:

Hello
world

The AI sees something like:

15339
1917


These numbers are token IDs.

Tokens are chunks of text.

Sometimes a token is:

a word
part of a word
punctuation
whitespace

The AI never sees "meaning."

It sees token sequences.

Think of it like this:

Humans hear music.

AI sees sheet music.

Chapter 3: The World's Most Expensive Autocomplete

People often think ChatGPT is a search engine.

It isn't.

People think it stores facts and retrieves them.

Not exactly.

At its core, it is:

A next-token prediction engine.

Imagine the sentence:

The capital of France is


What comes next?

Probably:

Paris


Now imagine doing that prediction not once, but trillions of times.

That's how LLMs learn.

The training objective is surprisingly simple:

Given:

The capital of France is


Predict:

Paris


Given:

2 + 2 =


Predict:

4


Given:

Once upon a


Predict:

time


Repeat this trillions of times.

The model slowly becomes smarter.

Chapter 4: The Transformer Revolution

Inside ChatGPT sits an architecture called:

Transformer

This invention changed AI forever.

Before Transformers, AI struggled with long pieces of text.

Transformers introduced a mechanism called:

Attention

Attention answers the question:

What parts of the previous text matter right now?

For example:

John went to the store.
He bought milk.


When processing "He", the model must figure out:

Who is "He"?

Attention lets it look backward.

It notices:

John


and connects the dots.

This tiny innovation created the foundation of:

GPT
Claude
Gemini
Llama
DeepSeek

Nearly every modern AI uses some variant of the Transformer.

Chapter 5: How Training Actually Happens

Now comes the expensive part.

The model starts completely random.

Every weight is random.

Its first predictions are nonsense.

Imagine asking:

2 + 2 =


and it replies:

Banana


That's roughly how bad it starts.

Then training begins.

For every example:

Predict next token
Compare prediction to reality
Calculate error
Slightly adjust billions of parameters
Repeat

Millions of times.

Billions of times.

Trillions of times.

Eventually the model discovers statistical patterns hidden in language.

Chapter 6: Where Intelligence Comes From

A fascinating question:

How can next-word prediction create intelligence?

Because language contains compressed knowledge.

To predict:

Einstein developed the theory of


you must know physics.

To predict:

The CEO of Tesla is


you must know people and companies.

To predict source code:

for(int i=0;


you must understand programming.

The AI isn't directly taught facts.

Instead it learns them because:

Accurate prediction requires understanding.

This is one of the most surprising discoveries in modern AI.

Chapter 7: Why ChatGPT Isn't Just GPT

After pretraining, the model becomes a:

Base Model

A base model can write.

But it isn't an assistant.

Ask it:

What is 2 + 2?


and it might continue like an internet article.

It doesn't necessarily answer.

It just continues text.

To transform it into ChatGPT, another stage is added.

Chapter 8: Teaching AI to Be Helpful

Humans now create conversations.

Example:

Human

What is 2 + 2?

Assistant

2 + 2 equals 4.

Thousands.

Millions.

Of conversations.

The model learns:

be helpful
answer questions
explain ideas
refuse harmful requests

This process is called:

Supervised Fine Tuning (SFT)

Think of it like sending the AI to customer-service training after university.

Chapter 9: What You're Really Talking To

This is one of the deepest ideas from the transcript.

Many people think:

"I'm talking to an AI mind."

A more accurate mental model is:

You're talking to a simulation of many expert human labelers.

The model learned from countless examples of how skilled humans answered questions.

When you ask ChatGPT something, the model predicts:

"What would an ideal assistant probably say next?"

That subtle distinction explains a lot.

Chapter 10: Hallucinations

Why does AI confidently invent fake facts?

Because prediction and truth are different things.

Suppose you ask:

Who is Orson Kovats?


And suppose that person doesn't exist.

The model still sees a familiar pattern:

Who is X?


During training that pattern is normally followed by:

X is a famous ...


So older models often invented biographies.

This phenomenon is called:

Hallucination

The AI isn't lying.

It's predicting.

And prediction sometimes creates fiction.

Chapter 11: Memory vs Context

A powerful insight:

LLMs have two kinds of knowledge.

Long-Term Memory

Stored inside model weights.

Like:

Paris is in France
Python is a language
Einstein was a physicist
Working Memory

Stored in the context window.

This is everything in the conversation.

Whatever you provide directly is more reliable than what the model remembers.

That's why professional prompting often means:

Give the model the information instead of hoping it remembers.

Chapter 12: Why AI Sometimes Looks Stupid

Here's the funny part.

LLMs can:

✅ write software

✅ solve advanced math

✅ explain quantum mechanics

But sometimes fail at:

❌ Counting letters

❌ Counting dots

❌ Spelling tricks

❌ Weird comparisons

Why?

Because they think in tokens, not characters.

Humans see:

strawberry


The AI may see:

straw
berry


as tokens.

Counting letters becomes surprisingly difficult.

This explains many famous AI mistakes.

Chapter 13: Why "Think Step By Step" Works

A fascinating limitation:

The model only does a limited amount of computation per token.

If you demand:

Give the answer immediately.

The AI has little room to reason.

But if you ask:

Think step by step.

The model creates intermediate thoughts.

Example:

2 oranges × $2 = $4
13 − 4 = 9
9 ÷ 3 = 3


Now reasoning is spread across tokens.

This makes difficult problems much easier.

That's why chain-of-thought prompting became so powerful.

Chapter 14: Tools Are Superpowers

Modern AI isn't limited to memory.

It can use tools.

Examples:

Search

The model can search the web.

Code Execution

The model can write Python and run it.

Calculations

Instead of mental math:

237,198 × 991


it can ask Python.

Document Analysis

It can read files directly.

Think of tools as:

Giving the AI a calculator, browser, notebook and microscope.

Chapter 15: The Rise of Reasoning Models

Then came a breakthrough.

Models like:

DeepSeek R1
OpenAI O-series
Gemini Thinking

use Reinforcement Learning.

Instead of merely copying human solutions:

They practice.

Just like students solving exercises.

The process:

Try many solutions
Check which succeed
Reward successful reasoning
Repeat

Over time, the model develops its own thinking strategies.

This is where modern reasoning AI comes from.

Chapter 16: The "Aha!" Moment

One shocking finding:

Reasoning models started saying things like:

"Wait, let me double-check."

"I might have made a mistake."

"Let's approach this differently."

These behaviors weren't explicitly programmed.

They emerged naturally during reinforcement learning because they improved accuracy.

It's similar to how good human thinkers review their work.

The model learned that careful thinking pays off.

Chapter 17: Why This Matters

The biggest lesson from the transcript is:

LLMs are neither magic nor simple autocomplete.

They are:

massive knowledge compressors
statistical reasoners
pattern learners
tool users
emerging problem solvers

But they are also:

imperfect
fallible
prone to mistakes
occasionally bizarre

The best mindset is:

Treat them as extremely capable collaborators, not infallible oracles.

Final Takeaway

If you remember only one thing from this entire book:

ChatGPT is not retrieving answers.

It is generating them.

Everything starts from predicting the next token.

From that simple objective emerged:

language understanding
coding ability
reasoning
translation
creativity
conversation

Modern AI is essentially a giant prediction engine that became intelligent by trying to predict humanity itself.

And that is what makes LLMs one of the most fascinating technologies ever created.