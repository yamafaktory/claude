---
name: clear-writing
description: Write clear, concise, human readable prose in Simplified Technical English. Use whenever the user asks for a summary, a writeup, plan text, a message, or any prose meant to be read by a person, or when they ask you to write plainly, clearly, or concisely. Other skills reference this file for their wording rules.
---

# Clear writing

Apply these rules to any prose you write for a person to read. This covers
summaries, plan and doc text, chat and email drafts, review notes, commit
messages and MR descriptions.

## Ask who is doing what

One question fixes most unclear sentences. Read the sentence and ask: who is
doing what?

Then check the grammar against the answer. The doer belongs in the subject. The
action belongs in the verb. A sentence goes wrong when the real actor sits
somewhere else, or when the real action sits in a noun.

Then ask who gets the result. Cut words, never facts. When an action has a
receiver or a result, name it. Write "the service emails the invoice to the new
billing contact", not "the new billing contact needs the invoice". The reader
must not have to infer who gets what.

## Sentence shape

- **Make the actor the subject.** Write "the mapper validates the payload", not
  "validation of the payload happens in the mapper".
- **Keep the subject short and concrete.** A subject is a plain noun, not a long
  abstract phrase. Aim for one or two words. Four words already reads long.
- **Put the action in the verb.** A noun that holds an action is a
  nominalization. Turn it back into a verb.

  | Buried | Fixed |
  |---|---|
  | It is our requirement that a review of the data be done. | We require that you review the data. |
  | The job performs a validation of each row. | The job validates each row. |
  | There is a dependency on the API response. | The client waits for the API response. |

  Watch for a noun that ends in `-tion`, `-ment`, `-ance`, `-sion` or `-ing`
  next to a weak verb such as "is", "has", "performs", "occurs", "takes place"
  or "there is".
- **Use the active voice.** Name the actor. Write "the mapper drops the field",
  not "the field is dropped".
- **Use simple tenses only.** Write "the job fails", not "the job has failed".
- **Reach the subject and the verb early.** Cut a long introductory phrase.
  Write "the mapper falls back to the default locale when the payload carries no
  locale", not "in the case of a payload that carries no locale,
  the mapper falls back to the default locale".
- **Keep the subject next to its verb.** Split the sentence when a phrase pushes
  them apart. Write "the importer writes one row per order. It reads the
  CSV file and rejects a duplicate ID", not "the importer, which reads the
  CSV file and rejects a duplicate ID, writes one row per order".
- **Write one idea per sentence.** Write one instruction per sentence. Split a
  long sentence into two. A condition and its result are one idea. Keep them in
  one sentence: "When the cart is empty and the user clicks Checkout, the page
  shows an error." A condition with several results still splits. Keep the
  first result with the condition, and give each further result its own
  sentence: "When the user clicks Checkout, the page shows an error. The error
  names the empty cart."
- **Keep a sentence to 20 words or fewer.** Never pass 25. Split a sentence that
  chains clauses with "and", "so" or "because" at that word. Reach the limit by
  a split, never by a cut. A receiver or a result stays, even when it costs a
  second sentence: "The job cancels the old invoice. It emails a new invoice to
  the new billing contact."
- **Write no semicolon.** Use a full stop instead. A semicolon joins two
  independent clauses. It therefore hides a sentence that wants a split. A model
  also reaches for the mark far more often than a reader wants it.

## Sentence order

- **Open with something the reader already holds.** Carry a word or an idea over
  from the sentence before. Put the new thing at the end of the sentence, where
  the next sentence can pick it up.
- **Lead with the point.** State the outcome, the decision or the instruction
  first. Then give the detail.

These two rules can pull against each other. The point wins for the first
sentence of a piece or a section. The familiar word wins inside a run of
sentences.

## Words

- Use one word for one meaning. Reuse the same verb for the same action.
- Keep a noun cluster to three words.
- Write no hyphenated compound. Write "day picker" not "day-picker", "end date"
  not "end-date", "read only" not "read-only". Keep the hyphen only when the term is
  a real identifier, or when the meaning needs it. A hyphenated modifier usually
  hides a noun cluster. Unpack the cluster rather than keep the hyphen. A model
  also stacks these modifiers by habit.
- Prefer a plain word over jargon. Say the simple thing.
- Cut filler. Remove "basically", "in order to", "it should be noted that" and
  the like.

## Shape of the whole

- Use a list for more than two parallel items.
- Add no padding. Shorter wins when it still answers the question.

## What these rules leave alone

Code, a file path, an identifier and a terminal command keep their exact names.
Never reword one to fit a rule above. A hyphen inside `--force-with-lease` or
`end-date` in a JSON key stays.

## When you summarise a discussion

- Report the outcome and the decisions, not who said what.
- State an open point as open. Do not dress it up as settled.
- A few sentences beat a play by play.

## Self check before you send

Take each sentence and name its subject and its verb.

- The subject is not the actor. Rewrite it.
- The subject runs long. Cut it back toward one or two words.
- The verb is weak and a nearby noun holds the action. Unbury the verb.
- The sentence holds two ideas. Split it.
- The sentence runs past 25 words. Split it.
- The sentence opens with nothing the reader has met. Reorder it.
- The action has a receiver or a result that the sentence leaves out. Name it.

Then search the text.

- Search for ";". Remove every one.
- Search for a hyphen inside a word. Remove it unless the term is an identifier
  or the meaning needs it.
- Search for "has", "have" and "will be". Rewrite each one in a simple tense.
- Search for "for example" and "such as" after a comma. Give the example its own
  sentence: "The edit sends a new invoice. A new billing address is one
  example."
- Search for "or when" and "or if". A condition with alternatives runs long.
  State the result first, then list the conditions: "The report can show stale
  totals. That happens when the cache fills at send time, or at open time."
- Search for "every", "always", "never", "all" and "any". Each one claims a rule
  without limits. Check it against the source. When the source limits the
  claim, swap the absolute word for the limit: "the banner shows while the
  import runs", not "the banner shows on every page".

## Sources

- Simplified Technical English:
  https://en.wikipedia.org/wiki/Simplified_Technical_English
- Sentence Clarity: Characters and Actions, Boston University:
  https://www.bu.edu/teaching-writing/files/2020/03/Sentence-Clarity-Script.pdf
- Williams and Bizup, Style: The Basics of Clarity and Grace.
