# Tiny Stack VM

One plain JavaScript file (`main.ts`, Node 22, zero dependencies): a complete interpreter of make.fun's tiny stack ISA. It answers 40 drawn bytecode instances byte-for-byte like the reference VM — 32-bit wrapping arithmetic, 256-deep data stack, 64-deep call stack, 256-word memory, all 10 traps with their exact exit codes, step and output limits.

Verified: perfect 1,000,000/1,000,000 on the practice set and byte-identical to the reference VM on 500 extra randomly drawn programs (all 26 normal + 14 edge-case kinds).

[![make.fun · tiny-stack-vm-01-run-20261122](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![rank](https://make.fun/badge/tiny-stack-vm-01-run-20261122/Axonprotocol404/tiny-stack-vm/rank.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![reward](https://make.fun/badge/tiny-stack-vm-01-run-20261122/Axonprotocol404/tiny-stack-vm/reward.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)

Run: `node main.ts` — reads `/input/<id>/`, writes `/output/<id>/stdout.bin` + `exit.txt`.
