xcompose-latex
==============

Generate entries to add to your XCompose from latex commands descriptions.

You should probably use a real mappings but this one could come handy.

Known issues
============

~~Problem: some entries are prefixes of others, making the former impossible to use, like "\ll" and "\lll". Maybe add a space at the end? That may be annoying to use.~~ Let's see how it goes with a space at the end of the sequence.

ASCII characters won't be recognized as candidates for special characters, that is probably for the best. However, if there are non `[A-Za-z0-9\t ]` characters in the source file, an insightful comment will be outputted instead of the XCompose command, allowing manual handling of the pathological case.

Example
=======

if you run it on the following file as standard input:

    Latex	 Symbol	 Description
    \in   ∈	 element of, sideways cup with horizontal bar, opening right
    \ni   ∋	 contains as member, reverse of \in
    \leq  ≤	 less or equal, represented by < over = signs
    \geq  ≥	 greater or equal, represented by > over = signs
    \ll   ≪	 much less, represented by 2 < in a row
    \gg   ≫	 much greater, represented by two > in a row
    \prec ≺	 precedes, < with both lines curving outward
    \succ ≻	 succeeds, reverse of \prec

then the output would be:

    <Multi_key> <backslash> <i> <n> <space> : "∈"  # latex \in
    <Multi_key> <backslash> <n> <i> <space> : "∋"  # latex \ni
    <Multi_key> <backslash> <l> <e> <q> <space> : "≤"  # latex \leq
    <Multi_key> <backslash> <g> <e> <q> <space> : "≥"  # latex \geq
    <Multi_key> <backslash> <l> <l> <space> : "≪"  # latex \ll
    <Multi_key> <backslash> <g> <g> <space> : "≫"  # latex \gg
    <Multi_key> <backslash> <p> <r> <e> <c> <space> : "≺"  # latex \prec
    <Multi_key> <backslash> <s> <u> <c> <c> <space> : "≻"  # latex \succ
