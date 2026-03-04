# SoloPistol vs gaju33333 (SoloPistol POV)

- White: `gaju33333`
- Black: `SoloPistol`
- POV: `SoloPistol` (Black)
- Turn labels: `me` = `SoloPistol`, `op.` = `gaju33333`

## Significant Swings

- Config: threshold=20.0 pts, scope=pov, max-events=8, cause-mode=forensic

- [Major] 2... Nf6 (me): W/L/D 0.2/2.6/97.2 -> 0.0/44.5/55.5, eval -0.24 -> -0.89, expected score 0.49 -> 0.28 (-21.1 pts)
  Impact: me=negative (-21.1 pts), op.=positive (+21.1 pts)
  Best: a6 (Stockfish) | Played: Nf6 | Opportunity cost: 0.68 pawns worse
  Engines: Stockfish=0.68 pawns worse, Lc0=0.68 pawns worse, confidence=Medium
  Evidence: SF PV a6 Nge2 e6 g3 b5 Bg2 | Lc0 PV Nc6
  Cause: 2... Nf6 was inferior to a6; it was playable but less accurate than safer alternatives. Evidence: expected score 0.49 -> 0.28 (-21.1 pts), Stockfish 0.68 pawns worse, Lc0 0.68 pawns worse.
  What you likely thought: Humans often choose a reasonable plan without testing whether a cleaner move avoids future problems.
  What you missed on the board: Small improvements in safety and coordination were available. The practical risk came from move-order and safety checks, not from one obvious tactical shot.
  How to decide better next time: 1) Test one alternative move. 2) Compare safety after one opponent reply. 3) Pick the cleaner structure.
  Practice habit: In quiet positions, spend one extra check on piece safety and structure.
  Lesson: Precision in quiet moments prevents future tactical strain.


- [Major] 9... d6 (me): W/L/D 100.0/0.0/0.0 -> 0.6/0.5/98.9, eval 2.95 -> 0.02, expected score 1.00 -> 0.50 (-49.9 pts)
  Impact: me=negative (-49.9 pts), op.=positive (+49.9 pts)
  Best: d5 (Stockfish+Lc0) | Played: d6 | Opportunity cost: 5.92 pawns worse
  Engines: Stockfish=2.82 pawns worse, Lc0=9.03 pawns worse, confidence=Medium
  Evidence: SF PV d5 Bb5 d4 Bxc6 bxc6 Bxh6 | Lc0 PV d5
  Cause: 9... d6 was inferior to d5; it created a large practical drop compared with safer continuations. Evidence: expected score 1.00 -> 0.50 (-49.9 pts), Stockfish 2.82 pawns worse, Lc0 9.03 pawns worse.
  What you likely thought: Humans under time pressure often pick the first workable move instead of comparing two serious candidates. That shortcut is costly in sharp middlegames.
  What you missed on the board: The missed cue was decision quality, not only tactics: candidate comparison and safety checks were incomplete. After your move, the opponent also had 3 capture(s), increasing tactical volatility.
  How to decide better next time: 1) Pick two serious candidates. 2) Run a brief CCT scan for both sides on each. 3) Choose the line with fewer immediate tactical liabilities.
  Practice habit: Never play the first acceptable move in sharp positions; compare at least two candidates.
  Lesson: Candidate comparison prevents large practical blunders.


- [Critical] 10... Na5 (me): W/L/D 100.0/0.0/0.0 -> 0.1/2.5/97.4, eval 2.96 -> -0.28, expected score 1.00 -> 0.49 (-51.2 pts)
  Impact: me=negative (-51.2 pts), op.=positive (+51.2 pts)
  Best: d5 (Stockfish+Lc0) | Played: Na5 | Opportunity cost: 5.29 pawns worse
  Engines: Stockfish=2.93 pawns worse, Lc0=7.65 pawns worse, confidence=Medium
  Evidence: SF PV d5 Bb5 d4 Bxc6 bxc6 Bd2 | Lc0 PV d5
  Cause: 10... Na5 was inferior to d5; it created a large practical drop compared with safer continuations. Evidence: expected score 1.00 -> 0.49 (-51.2 pts), Stockfish 2.93 pawns worse, Lc0 7.65 pawns worse.
  What you likely thought: Humans under time pressure often pick the first workable move instead of comparing two serious candidates. That shortcut is costly in sharp middlegames.
  What you missed on the board: The missed cue was decision quality, not only tactics: candidate comparison and safety checks were incomplete. After your move, the opponent also had 3 capture(s), increasing tactical volatility.
  How to decide better next time: 1) Pick two serious candidates. 2) Run a brief CCT scan for both sides on each. 3) Choose the line with fewer immediate tactical liabilities.
  Practice habit: Never play the first acceptable move in sharp positions; compare at least two candidates.
  Lesson: Candidate comparison prevents large practical blunders.


- [Major] 11... Bd7 (me): W/L/D 51.8/0.0/48.2 -> 0.6/0.5/98.9, eval 0.97 -> 0.02, expected score 0.76 -> 0.50 (-25.8 pts)
  Impact: me=negative (-25.8 pts), op.=positive (+25.8 pts)
  Best: a6 (Stockfish+Lc0) | Played: Bd7 | Opportunity cost: 0.84 pawns worse
  Engines: Stockfish=0.87 pawns worse, Lc0=0.80 pawns worse, confidence=Medium
  Evidence: SF PV a6 Ba4 b5 Bb3 d5 e5 | Lc0 PV a6
  Cause: 11... Bd7 was inferior to a6; it was playable but less accurate than safer alternatives. Evidence: expected score 0.76 -> 0.50 (-25.8 pts), Stockfish 0.87 pawns worse, Lc0 0.80 pawns worse.
  What you likely thought: Humans often choose a reasonable plan without testing whether a cleaner move avoids future problems.
  What you missed on the board: Small improvements in safety and coordination were available. After your move, the opponent also had 3 capture(s), increasing tactical volatility.
  How to decide better next time: 1) Test one alternative move. 2) Compare safety after one opponent reply. 3) Pick the cleaner structure.
  Practice habit: In quiet positions, spend one extra check on piece safety and structure.
  Lesson: Precision in quiet moments prevents future tactical strain.


- [Critical] 13... d5 (me): W/L/D 1.0/0.3/98.7 -> 0.0/100.0/0.0, eval 0.11 -> -4.58, expected score 0.50 -> 0.00 (-50.4 pts)
  Impact: me=negative (-50.4 pts), op.=positive (+50.4 pts)
  Best: dxe5 (Stockfish+Lc0) | Played: d5 | Opportunity cost: 11.21 pawns worse
  Engines: Stockfish=4.78 pawns worse, Lc0=17.64 pawns worse, confidence=Medium
  Evidence: SF PV dxe5 Nxe5 | Lc0 PV dxe5
  Cause: 13... d5 was inferior to dxe5; it missed a tactical resource and allowed avoidable material damage. Evidence: expected score 0.50 -> 0.00 (-50.4 pts), Stockfish 4.78 pawns worse, Lc0 17.64 pawns worse.
  What you likely thought: Humans often lock onto one plan and fail to refresh candidate moves after the position changes. That causes tactical resources to be overlooked.
  What you missed on the board: The missed cue was tactical forcing order: checks and captures changed the material outcome quickly. After your move, the opponent also had 4 capture(s), increasing tactical volatility.
  How to decide better next time: 1) Rebuild candidate moves from scratch. 2) Prioritize forcing moves before quiet plans. 3) Compare resulting material after each forcing branch.
  Practice habit: When the position is tactical, restart candidate generation every move.
  Lesson: In tactical positions, forcing move order decides material outcomes.


- [Critical] 29... Qb8 (me): W/L/D 73.5/0.0/26.5 -> 0.0/100.0/0.0, eval 1.17 -> -4.47, expected score 0.87 -> 0.00 (-86.8 pts)
  Impact: me=negative (-86.8 pts), op.=positive (+86.8 pts)
  Best: Nc5 (Stockfish+Lc0) | Played: Qb8 | Opportunity cost: 14.94 pawns worse
  Engines: Stockfish=5.42 pawns worse, Lc0=24.47 pawns worse, confidence=Medium
  Evidence: SF PV Nc5 Rc1 Qf8 Qd5+ Kh8 g4 | Lc0 PV Nc5
  Cause: 29... Qb8 was inferior to Nc5; it missed a tactical resource and allowed avoidable material damage. Evidence: expected score 0.87 -> 0.00 (-86.8 pts), Stockfish 5.42 pawns worse, Lc0 24.47 pawns worse.
  What you likely thought: Humans often lock onto one plan and fail to refresh candidate moves after the position changes. That causes tactical resources to be overlooked.
  What you missed on the board: The missed cue was tactical forcing order: checks and captures changed the material outcome quickly. After your move, the opponent had 5 checking idea(s), which is a forcing-warning signal. After your move, the opponent also had 3 capture(s), increasing tactical volatility.
  How to decide better next time: 1) Rebuild candidate moves from scratch. 2) Prioritize forcing moves before quiet plans. 3) Compare resulting material after each forcing branch.
  Practice habit: When the position is tactical, restart candidate generation every move.
  Lesson: In tactical positions, forcing move order decides material outcomes.

```text
Ply   Turn Move    Win% Loss% Draw%    Eval
-------------------------------------------
1.    op. e4       0.2   2.8  97.0   -0.25
1...  me  c5       0.1   7.5  92.4   -0.45
2.    op. Nc3      0.2   2.6  97.2   -0.24
2...  me  Nf6      0.0  44.5  55.5   -0.89
3.    op. Nf3      0.1   6.7  93.2   -0.44
3...  me  Nc6      0.0  10.3  89.7   -0.53
4.    op. Bc4      0.8   0.6  98.6    0.03
4...  me  e6       0.6   0.8  98.6   -0.02
5.    op. d3       1.9   0.2  97.9    0.20
5...  me  Bd6      0.0  10.0  90.0   -0.53
6.    op. Bg5      6.4   0.1  93.5    0.44
6...  me  Be7      0.9   0.4  98.7    0.07
7.    op. O-O      1.1   0.3  98.6    0.11
7...  me  O-O      0.6   0.6  98.8    0.00
8.    op. h3       0.8   0.4  98.8    0.06
8...  me  h6       0.7   0.4  98.9    0.04
9.    op. Be3    100.0   0.0   0.0    2.95
9...  me  d6       0.6   0.5  98.9    0.02
10.   op. a3     100.0   0.0   0.0    2.96
10... me  Na5      0.1   2.5  97.4   -0.28
11.   op. Bb5     51.8   0.0  48.2    0.97
11... me  Bd7      0.6   0.5  98.9    0.02
12.   op. Bxd7     0.8   0.3  98.9    0.07
12... me  Qxd7     0.8   0.3  98.9    0.08
13.   op. e5       1.0   0.3  98.7    0.11
13... me  d5       0.0 100.0   0.0   -4.58
14.   op. exf6     0.0 100.0   0.0   -4.29
14... me  Bxf6     0.0 100.0   0.0   -4.67
15.   op. Bxc5     0.0 100.0   0.0   -4.49
15... me  Qc6      0.0 100.0   0.0   -5.53
16.   op. Bxf8     0.0 100.0   0.0   -5.40
16... me  Rxf8     0.0 100.0   0.0   -5.48
17.   op. d4       0.0 100.0   0.0   -5.31
17... me  Nc4      0.0 100.0   0.0   -5.28
18.   op. Nd2      0.0 100.0   0.0   -3.06
18... me  Nxb2     0.0 100.0   0.0   -3.41
19.   op. Qf3      0.0 100.0   0.0   -3.23
19... me  Bxd4     0.0 100.0   0.0   -3.41
20.   op. Ne2      0.0 100.0   0.0   -3.16
20... me  Bb6      0.0 100.0   0.0   -3.82
21.   op. Rac1     0.0 100.0   0.0   -3.50
21... me  f5       0.0 100.0   0.0   -4.66
22.   op. c4       0.0 100.0   0.0   -4.55
22... me  Rd8      0.0 100.0   0.0   -5.18
23.   op. cxd5     0.0 100.0   0.0   -4.39
23... me  Qd6      0.0 100.0   0.0   -5.60
24.   op. Rc2      0.0 100.0   0.0   -5.33
24... me  Na4      0.0 100.0   0.0   -5.47
25.   op. dxe6     0.0 100.0   0.0   -5.30
25... me  Qxe6     0.0 100.0   0.0   -5.56
26.   op. Qxb7     0.0 100.0   0.0   -3.08
26... me  Qxe2     0.0 100.0   0.0   -3.35
27.   op. Rc8      5.2   0.0  94.8    0.46
27... me  Qxd2     3.4   0.1  96.5    0.38
28.   op. Rxd8+   56.5   0.0  43.5    1.03
28... me  Qxd8    67.8   0.0  32.2    1.12
29.   op. Qc6     73.5   0.0  26.5    1.17
29... me  Qb8      0.0 100.0   0.0   -4.47
30.   op. Qxa4     0.0 100.0   0.0   -4.45
30... me  Qe5      0.0 100.0   0.0   -4.63
31.   op. Qb4      0.0 100.0   0.0   -4.39
31... me  Bc7      0.0 100.0   0.0   -4.71
32.   op. g3       0.0 100.0   0.0   -4.47
32... me  f4       0.0 100.0   0.0   -5.47
33.   op. Qc4+     0.0 100.0   0.0   -5.02
33... me  Kh7      0.0 100.0   0.0   -5.35
34.   op. Qxc7   100.0   0.0   0.0    5.29
34... me  Qxc7   100.0   0.0   0.0    5.30
```
