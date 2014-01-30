xcompose-latex
==============

Generate entries to add to your XCompose from latex commands descriptions.

You should probably use a real mappings but this one could come handy.

Known issues
============

Problem: some entries are prefixes of others, making the former impossible to use, like "\ll" and "\lll". Maybe add a space at the end? That may be annoying to use.

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

    <Multi_key> <backslash> <i> <n> : "∈"  # latex \in
    <Multi_key> <backslash> <n> <i> : "∋"  # latex \ni
    <Multi_key> <backslash> <l> <e> <q> : "≤"  # latex \leq
    <Multi_key> <backslash> <g> <e> <q> : "≥"  # latex \geq
    <Multi_key> <backslash> <l> <l> : "≪"  # latex \ll
    <Multi_key> <backslash> <g> <g> : "≫"  # latex \gg
    <Multi_key> <backslash> <p> <r> <e> <c> : "≺"  # latex \prec
    <Multi_key> <backslash> <s> <u> <c> <c> : "≻"  # latex \succ
