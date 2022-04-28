# Match Line

* Negative Match Line [stackoverflow-reference](https://stackoverflow.com/questions/1240275/how-to-negate-specific-word-in-regex#answer-1240293)
- Look ahead : ^(?!.*?bar).*
- Look behind : ^(.(?<!bar))*?$
- Line not containing : ^(?!.*TEXT-TO-NOT-MATCH).*\n
