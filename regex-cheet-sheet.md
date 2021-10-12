  
# Match Line

* Negative Match Line [reference](https://stackoverflow.com/questions/1240275/how-to-negate-specific-word-in-regex#answer-1240293)
  * Look ahead : ^(?!.*?bar).*
  * Look behind : ^(.(?<!bar))*?$
