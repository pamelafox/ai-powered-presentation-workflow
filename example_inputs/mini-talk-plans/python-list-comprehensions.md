# Mini talk plan: How Python list comprehensions work

## Audience

Python beginners who can already write `for` loops and create lists, but have seen list comprehensions and found them hard to read.

## Goal

By the end, the audience should understand how a list comprehension maps from a normal `for` loop into a compact expression, and when to use one.

## Constraints

- 3 to 5 minutes
- 4 to 6 slides
- Include one concrete example
- Use simple speaker notes

## Draft outline

1. Why list comprehensions exist
2. Start with a normal `for` loop
3. Transform the loop into a list comprehension
4. Add a simple filter with `if`
5. Final takeaway: use them for readable transformations

## Speaker-note guidance

- Emphasize that list comprehensions are not magic syntax; they are a compact way to build a list from another iterable.
- Use one example throughout, such as converting numbers to squares or cleaning a list of names.
- Warn against making list comprehensions too clever. If it is hard to read, use a regular loop.
