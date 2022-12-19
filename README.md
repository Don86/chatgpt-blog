# About `chatGPT`

### 19 Dec 2022

Started this blog to write my thoughts, publicly available to anyone who cares. PS: at the time of this writing, I have not tried `copilot`. 

**Short term limitations**

This is mostly from my experience attempting to write a linting script for data folders before ingestion, using `PowerShell`, which I have no knowledge of. It really just has checks like "must have at least 1 file named like `*_final.xls`, `*_final.xlsx` or `*_final.csv`", and maybe half a dozen other such conditions to look out for. Piece of piss, right? 

The [door problem](https://www.gamedeveloper.com/design/-quot-the-door-problem-quot-of-game-design), again - `cgpt` makes some assumptions about your input. In the obvious case, a prompt like "python function to calculate Fibonacci sequence" will return a script that calculates, for example, the first *n* members of the Fibonacci sequence, because attempting to print out the entire Fib sequence is a non-terminating function. In the same way, `cgpt` is *less* fragile to producing what seems like a workable output (even assuming that the code it produces is 100% correct), but the utility of script-as-you-go is precisely because it's *more* fragile, and forces the dev to think through as many scenarios as possible, other than the happy path, in order to arrive at a working output at all. 

However, I have little doubt that `cgpt` will soon be able to generate nearly 100% correct simple scripts within 5 years or so. Either than or the dev-UX undergoes some serious improvement. At least this might encourage the practice where one writes the unit test first before writing the function. 

**Long Term Predictions**

`cgpt` could go one of two ways:

1. The better scenario for SWEs: no one other than an SWE could really use `cgpt`. Simple scripts can now be handed over to the AI, but what's considered "simple" has always been relative anyway (and heavily subject to the intelligence of the dev in question). This just increases the floor of complexity, the same way that we no longer have to use punch cards (admittedly, all those dedicated card punchers are all part of a job, having been replaced by compilers), but it's not like we stopped using computers. 
2. The worse scenario (for all humans, I think): machines becomes smart enough to decide for a user which system, out of all possible configurations of every possible stack, is the superior one, for a given prompt. 

* The best operating model of "AI"/ML so far has been a highy transparent model/stack, with humans to check and verify outputs/predictions at cognitively-feasible (i.e. dumbed down) checkpoints, instead of entirely hands-free automation. 

* Over the last several decades, simplification in tech has only brought about all new layers of complexity built upon this simplification. This isn't a phenomenon specific to tech; our ships, houses, bridges and so on became more complex as our tools became better. Once upon a time, websites were made of `html` files, now they're made of dependencies; web frameworks did not decrease the complexity of web dev. K8s and containerization seemed to simplify orchestration (*hey bro I heard you like config files so here's even more config files for your config files*), but now infra provision (or, more likely, productionization) is a whole giant headache in itself. 

* Once `cgpt` finally gets better at scripting, the language wars may finally end. Indeed, we might see specialty languages proliferate, and a need arise for compatibility (or some sort of glue) between languages, to stitch them together into an optimally performant app. This I'm actually quite excited to see. 
