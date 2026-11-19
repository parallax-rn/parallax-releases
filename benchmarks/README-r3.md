# Benchmark R3: four setups on interaction bugs (pre-registration)

R3 compares four ways to give a coding agent a React Native app on the iOS simulator, on bugs that need a gesture to reproduce the bug or to check the fix. The gestures are a scroll to an element off screen, a swipe on a row, a drag to reorder, a long press, a pull to refresh, a pan on a photo, and a scroll through a list with a stale stored value.

The four setups (arms) are R1's:
- A0: a shell with AXe only;
- A1: agent-device;
- A2: Argent;
- A3: Parallax.

Each setup uses the tool's own official setup in an isolated config. The agent is the same in all four: Claude Code with Claude Sonnet 5.5, headless.

There are seven gesture tasks (G1 to G7) and two controls (C1, B4) on a small shop app built with React Native core gestures. Each gesture task runs 3 times per arm, each control once per arm. The tasks are named only by id here. Their keys and the bug code stay private until the results are published.

**What we measure.** In order:
1. cost and cost per fix;
2. fixes, including fixes the agent checked on the device itself;
3. failed and repeated gesture calls;
4. wrong-target actions;
5. confident wrong answers.

**Versions.** The cut-off day is the day this file is published. Just before the first counted run, every tool is pinned to the version its npm `latest` points to; AXe is pinned to its latest GitHub release. A release published before the pin is the one tested. The method went to the agent-device and Argent maintainers before the first counted run. If one of their remarks changes a setup, the affected cells are run again, and the report lists it as a deviation.

`r3-prereg.json` holds the rules and the thresholds that would falsify each hypothesis. It was frozen on 2026-11-18, before the first counted run (sha256 2dbc9f03611de427851f82d5e425bc4030d930e1279c21bb135c98473a6dbfe8).
