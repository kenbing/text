### Sequence Points

***ISO standard says that you are not allowed to change a variable more than once (or
change and use one) without an intervening sequence point.**

There is no sequence point between the use of ```i``` in ```a[i]``` and the change of
```i``` in ```i++```.

*The list of sequence points from C11 (not really changed that much since C99) are
describe in Annex C:*

- Between the evaluations of the funciton designator and actual arguments in a function
call and the actual calll.
- Between the evaluations of the first and second operands of the following operators:
logical AND &&; logical OR ||; comma ,.
- The end of a full declarator: declarators;
- Between the evaluation of a full expression and the next full expression to be
evaluated. The following are full expressions: an initializer; the expression in an
expression statement; The controlling expression of a selection statement (if or
switch); the controlling expression of a while or do statement; each of the expressions
of a for statement; the expression in a return statement.
- After the actions associated with each formatted input/output function conversion
specifier.
- Immediately before and immediately after each call to a comparison function, and also
between any call to a comparison function and any movement of the objects passed as
arguments to that call.
