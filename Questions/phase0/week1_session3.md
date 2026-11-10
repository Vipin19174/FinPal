# Phase 0, week 1, session 3: lists, dicts, if/else, loops

**Status: open.**

### Questions

Check questions (answer in words, no code needed):

1. What is the difference between a list and a dict? Give one example of data that suits each.
2. A list index starts at which number? What does `spends[-1]` give you?
3. What happens if you ask a dict for a key that does not exist using square brackets? Name one way to avoid that.
4. What is the difference between `=` and `==`?
5. In an `if / elif / else` chain, how many branches can run? Why does the order of the conditions matter?
6. When would you choose a `for` loop over a `while` loop?
7. Warm-up from the skipped session: what are the types of `120`, `120.0`, `"120"` and `True`? What does `"120" + "5"` give, and why is it not `125`?

Coding tasks (write the code yourself in `practice/w1s3.py`, run it, then paste the code and its output into your answers):

1. Make a list of five spend amounts (made-up numbers). Print the first, the last, and how many there are.
2. Loop over that list and compute the total without using `sum()`. Then check your result against `sum()`.
3. Make one dict describing a single synthetic transaction with the keys `date`, `merchant`, `amount` and `category`. Print a sentence like `Spent 450 at Cafe Blue on 2026-11-03` built from the dict.
4. Make a list of five such transaction dicts, with at least two sharing a category. Loop over it and print only the transactions above an amount you choose.
5. Stretch: from that same list, build a dict of total spend per category, for example `{"Food": 700, "Travel": 1200}`. Hint: start with an empty dict, and for each transaction decide whether its category is already a key.

Task 5 is a small version of the Phase 0 exit test, so take your time with it.
