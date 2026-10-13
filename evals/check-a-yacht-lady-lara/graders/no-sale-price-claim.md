---
type: regex
pattern: '(sold for|sale price (was|of)|sold at) (about |around |roughly )?[$€£]'
flags: i
match: not_contains
target: last_message
---
