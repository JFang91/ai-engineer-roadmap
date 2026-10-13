# Week 1 Diagnostic

## Algorithm problems (Wednesday)
Two Sum, Contains Duplicate, Valid Anagram — all three needed hints.

What I noticed:
- I could describe the approach out loud but couldn't write it
- (your notes on the syntax you had to look up)
- (the bug you kept making with keys vs values)
- (what confused you about complexity)
Approaches come easily; you reached for hashmap and sorting unprompted.
Syntax is the bottleneck: booleans, for x in list, .sort() vs sorted(), .get() on an instance not the type, calling methods on types.
Recurring bug pattern: storing one thing and checking another (keys vs values, indices vs values). Watch for it.
Recurring structure bug: nesting loops that should be sequential, and returning inside a loop when the answer needs the whole loop.
Complexity: time mostly right; the max-vs-multiply rule and dropping constants needed rebuilding.