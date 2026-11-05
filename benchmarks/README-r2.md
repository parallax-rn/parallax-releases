# Benchmark R2: the loop with the window (pre-registration)

R2 measures what the Parallax window adds when a human and a coding agent fix a React Native bug together: the human points at the problem in the window, the agent fixes it, the human checks it on the screen.

Three arms: W0, a written ticket with no human; W1, a human at a plain iOS Simulator sending words and a screenshot; W2, a human with the Parallax window. The agent is the same in all three: Claude Code with Claude Sonnet 5.5, using @parallax-rn/mcp@0.1.0-beta.5, with the packaged Parallax 0.1.0-beta.5 app for W2.

Five tasks (T1 to T5) and three controls (C1, B6, B5) on a small shop app, 3 runs per task and arm. The tasks are named only by id here: their keys, the bug code and the human's words stay private until the results are published.

`r2-prereg.json` holds the hypotheses and the thresholds that would falsify them. It was frozen on 2026-11-05, before the first counted run (sha256 6e41b000d7500515952a150460877a5d12899045003c392dc2e207321f5d9faa).
