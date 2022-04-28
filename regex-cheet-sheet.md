# Basics
## Group
- Grouping : ```(match)some(pattern)```
  - Use Groups in Replacement
    - ```\1``` more ```\2```
    - ```$1``` more ```$2```

# Examples and Snippets
## Negative Match Line [stackoverflow-reference](https://stackoverflow.com/questions/1240275/how-to-negate-specific-word-in-regex#answer-1240293)
- Look ahead for "bar" : ```^(?!.*?bar).*```
- Look behind for "bar" : ```^(.(?<!bar))*?$```
- Line not containing "bar" (General) : ```^(?!.*bar).*\n```
