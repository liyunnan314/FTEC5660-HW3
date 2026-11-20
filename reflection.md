# Task 2: Reflection on AI-sycophancy and AI-psychosis

The most deliberate decision I made this homework was to keep the model out of
the verdict. My agent computes the three ratios with SQL, compares them against
the industry medians in Python, and only after the PASS or FAIL is fixed does
the model get to say anything — and even then it only writes the summary.

I did that because I was afraid of what the model would do if I let it judge. A
"worthwhile profit margin" is a vague phrase, and a model asked to say whether a
company clears it will, I suspected, lean toward saying yes. Most companies in
the data do pass, "this is a promising company" is the more agreeable answer,
and the grading metric itself punishes answering PASS everywhere. So I took the
judgement away from it entirely and left the model with nothing to do but
narrate.

What I did not expect is that the sycophancy did not disappear. It just moved.

Look at what the model does in the summary step. I hand it a verdict that has
already been decided — "Ashgrove fails the new-product test" — and it writes two
sentences explaining why that is a sensible, considered conclusion. It never
questions the verdict, never says "actually this is close". It does not know the
cutoff, or why 2023 was chosen, or that the whole thing is a rule I made up
yesterday. But the paragraph it produces reads like the product of careful
analysis. The model will defend any verdict I give it, PASS or FAIL, with the
same unearned confidence.

That is a sycophancy I find more worrying than the familiar "agreeing with the
user" kind. It is not the model agreeing with me. It is the model agreeing with
whatever conclusion is placed in front of it, and manufacturing the reasoning to
fit. When the reasoning arrives after the verdict, the reasoning is decoration.
Reading its summaries, I cannot tell which sentences came from evidence and
which were reverse-engineered to justify a foregone conclusion, because the
prose gives no sign.

Then there is the other side of it, which the assignment calls psychosis. The
companies here are fictional on purpose, so the model cannot answer from
memory. That is a quiet admission that, given the chance, it would. If I had
built an agent that was supposed to "research" a company without the SQL tool,
it would have produced revenue figures, growth rates and margin numbers for a
company that does not exist, formatted the way such numbers always look,
probably with a percentage sign and a comparison to an industry. It would have
been internally consistent, professionally worded, and entirely invented.

The two failures feel different but come from the same place. Sycophancy bends
the answer toward what the listener wants to hear; psychosis bends it toward
the story the model has already started telling. Both produce output that feels
right, and both outsource the question of whether it is true to a process that
is not actually checking. A fluent, confident answer is dangerous precisely
because nothing about fluency tells you whether it is true.

What I take from the week is that the reliability of an agent is not a property
of how well the model writes. It is a property of what the model's claims are
anchored to. My three points work because every verdict is anchored to a number
I can check in a database, and the model's summaries can say whatever they like
without moving the answer. Where a claim has to be justified by the model on its
own, sycophancy and psychosis are both waiting there.
