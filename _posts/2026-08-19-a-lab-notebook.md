---
title: A lab notebook, on the web
description: Why this site now has a blog, and what I plan to write down here.
date: 2026-08-19
tags:
  - notes
---

This site started as a single-page portfolio. That is still the front door. The blog is a place to write things down that do not belong on a résumé card: how a measurement was actually made, what broke, and what I would do differently next time.

I work on electron-beam metrology systems. The interesting part is rarely the headline number. It is the chain underneath — source, column, stage, detector, model, and the statistics that decide whether a result is real.

## What you will find here

- Notes from building and calibrating precision hardware
- Short write-ups on nanophotonics and inverse design when I have something concrete
- Occasional systems-engineering asides: interfaces, error budgets, and why “it works on my bench” is not a spec

I am not aiming for a publication venue. If a note is useful to one other person who has stared at a noisy residual and wondered whether the tool or the sample is lying, that is enough.

> Precision is a social contract with the next engineer who has to trust your number.

A typical first check when something drifts is embarrassingly small:

```python
residual_nm = measured_nm - model_nm
print(residual_nm.std())
```

If the scatter is honest, you can talk about the mean. If it is not, you go back to the instrument.

More soon.
