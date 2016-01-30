# composable-logic-js

This is an idea for a potential JavaScript library that supports chainable and composable boolean logic or other operators. Sometimes this is more terse than raw logic expressions, especially if you want to repeat terms or operator-term pairs.

```js
// functional style:
val(eq(or(apple, banana), coconut));
// or pure fluent style:
l(apple).or(banana).eq(coconut).val();
// is equivalent to:
// apple == coconut || banana == coconut

// functional style:
val(and(or(and(x, y), z), xor(p, q)));
// or pure fluent style:
l(l(l(x).and(y)).or(z)).and(l(p).xor(q)).val();
// or some hybrid
```
