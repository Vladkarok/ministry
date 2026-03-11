# Secretary Queue Timer

A single-file tool that estimates **when you'll receive the Secretary buff** when the main auto-appointment queue is full and you're waiting in the additional (overflow) queue.

## How it works

- The main auto-appointment queue holds **50 players**, each serving **5 minutes**
- When the main queue is full and you're in the **additional queue**, there's no built-in ETA shown
- This tool calculates it for you

Enter the number of people ahead of you in the additional queue. Optionally enable the toggle and enter the **current player's time in office** (MM:SS, shown in-game) for a precise estimate — otherwise a ±2:30 approximation is used.

The estimated buff time is locked the moment you enter your values. A live countdown ticks toward that fixed target.

## Languages

EN · UA · FR — toggle in the top-right corner. Choice is saved in `localStorage`.

## The math

```
estimated buff time = now
  + remaining time for current player  (exact or ~2:30)
  + 50 main queue players × 5 min
  + N additional queue players × 5 min
```
