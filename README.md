# Tiny Stack VM

A complete interpreter of make.fun's tiny stack ISA in one plain JavaScript file (`main.ts`, ~4.4 KB, Node 22, zero dependencies). It answers 40 drawn bytecode instances byte-for-byte like the reference VM: 32-bit wrapping arithmetic (`MUL` via exact low-32 product), 256-deep data stack, 64-deep call stack, 256-word memory, signed/unsigned division edge cases (`-2147483648 / -1`, remainder sign), arithmetic vs logical shifts, PUSH8 sign extension, all 10 traps with their exact exit codes, the 1,000,000-step and 65,536-byte output limits, input exhaustion, and falling off the program's end.

Verified: perfect 1,000,000/1,000,000 on the practice set and byte-identical against the reference VM on 500 additional randomly drawn programs (all 26 normal kinds + 14 edge-case kinds).

[![make.fun · tiny-stack-vm-01-run-20261122](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![rank](https://make.fun/badge/tiny-stack-vm-01-run-20261122/Axonprotocol404/tiny-stack-vm/rank.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)
[![reward](https://make.fun/badge/tiny-stack-vm-01-run-20261122/Axonprotocol404/tiny-stack-vm/reward.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)

Run: `node main.ts` — reads `/input/<id>/program.bin` + `input.bin`, writes `/output/<id>/stdout.bin` + `exit.txt`.
