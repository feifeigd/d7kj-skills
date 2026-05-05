---
# Roll Dice Skill
name: roll-dice
description: >
  Roll dice using a random number generator. Use when asked to roll a die (d6, d20, etc.), roll dice, or generate a random dice roll.
<!-- disable-model-invocation: true -->
---

To roll a die, use the following command that generates a random number from 1 to the given number of sides:

```bash
echo $((1 + RANDOM % <sides>))
```

```powershell
Get-Random -Minimum 1 -Maximum (<sides> + 1)
```

Replace `<sides>` with the number of sides on the die (e.g., 6 for a d6, 20 for a d20).

Example usage:
- "Roll a d6" → `echo $((1 + RANDOM % 6))`
- "Roll 3d10" → Generate three random numbers from 1 to 10 and sum them up:
```bash 
total=0; for i in {1..3}; do total=$((total + 1 + RANDOM % 10)); done; echo $total
```
```powershell
$total = 0; for ($i = 1; $i -le 3; $i++) { $total += Get-Random -Minimum 1 -Maximum 11 }; $total
```
This skill can be invoked when the user asks to roll a die or generate a random dice roll. It supports rolling multiple dice and summing their results.
