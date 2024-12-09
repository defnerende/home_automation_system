The state table for system_1 is given below.

| Current State   | Input (x) | Next State   | Output (y) |
|-----------------|-----------|--------------|------------|
| 0               | 0         | 0            | 0          |
| 0               | 1         | 1            | 1          |
| 1               | 0         | 0            | 0          |
| 1               | 1         | 1            | 1          |

Here, the current state of 1 represents that lights are on, and 0 represents that lights are off.

---------------------------------------------------------------------------------
The state table for system_2 is given below.

| Current State   | Input (x) | Next State   | Output (y) |
|-----------------|-----------|--------------|------------|
| 0               | 0         | 0            | 0          |
| 0               | 1         | 1            | 1          |
| 1               | 0         | 0            | 0          |
| 1               | 1         | 1            | 1          |

Here, the current state of 1 represents that someone is at home, and 0 represents that no one is at home.

---------------------------------------------------------------------------------

THe state table for system_3 is given below.

| Current State       | x1 (Lux) | x2 (Time) | Next State          | Output (y1, y2) |
|---------------------|----------|-----------|---------------------|-----------------|
| S0                  | 0        | 0         | S0                  | 0, 0           |
| S0                  | 0        | 1         | S1                  | 1, 0           |
| S0                  | 1        | 0         | S0                  | 0, 0           |
| S0                  | 1        | 1         | S2                  | 0, 1           |
| S1                  | 0        | 0         | S0                  | 0, 0           |
| S1                  | 0        | 1         | S1                  | 1, 0           |
| S1                  | 1        | 0         | S0                  | 0, 0           |
| S1                  | 1        | 1         | S2                  | 0, 1           |
| S2                  | 0        | 0         | S0                  | 0, 0           |
| S2                  | 0        | 1         | S1                  | 1, 0           |
| S2                  | 1        | 0         | S0                  | 0, 0           |
| S2                  | 1        | 1         | S2                  | 0, 1           |



Here, S0 represents the state where lights off and curtains are closed.

S1 reperesents the state where lights are on and curtains are closed.

S2 represents the state where lights are off and curtains are open.

y1 reperesents the state of lights.

y2 represents the state of curtains.

---------------------------------------------------------------------------------

The state table for system_4 is given below.

| Current State | x1  | x2  | Next State | Plant A | Plant B | Plant C | Plant D |
|---------------|-----|-----|------------|---------|---------|---------|---------|
| Monday        | 0   | 0   | Tuesday    | 1       | 0       | 1       | 0       |
| Tuesday       | 0   | 1   | Wednesday  | 0       | 1       | 0       | 0       |
| Wednesday     | 1   | 0   | Thursday   | 1       | 0       | 0       | 1       |
| Thursday      | 1   | 1   | Friday     | 0       | 0       | 1       | 0       |
| Friday        | 0   | 0   | Saturday   | 1       | 1       | 0       | 0       |
| Saturday      | 0   | 1   | Sunday     | 0       | 0       | 0       | 0       |
| Sunday        | 1   | 0   | Monday     | 0       | 0       | 0       | 0       |

Here x1 and x2 form the days of the week as follows: 

Monday: 00 → x1 = 0, x2 = 0

Tuesday: 01 → x1 = 0, x2 = 1

Wednesday: 10 → x1 = 1, x2 = 0

Thursday: 11 → x1 = 1, x2 = 1

Friday: 00 → x1 = 0, x2 = 0

Saturday: 01 → x1 = 0, x2 = 1

Sunday: 10 → x1 = 1, x2 = 0

---------------------------------------------------------------------------------

The state table for system_5 is given below. 



| Current State | P0, P1, P2, P3 | FR  | MO  | Next State | Door_lock Output |
|---------------|----------------|-----|-----|------------|------------------|
| S0            | 0000           | 0   | 0   | S0         | 0                |
| S0            | 0000           | 0   | 1   | S2         | 1                |
| S0            | 1111           | 1   | 0   | S1         | 1                |
| S0            | 1111           | 1   | 1   | S0         | 0                |
| S0            | 1111           | 0   | 1   | S2         | 1                |
| S1            | 1111           | 1   | 0   | S1         | 1                |
| S1            | 1111           | 1   | 1   | S2         | 1                |
| S2            | 0000           | 0   | 1   | S2         | 1                |
| S2            | 1111           | 1   | 0   | S0         | 0                |
| S2            | 1111           | 1   | 1   | S2         | 1                |
| S0            | 0001           | 0   | 1   | S2         | 1                |
| S0            | 1010           | 1   | 0   | S0         | 0                |
| S0            | 1010           | 1   | 1   | S2         | 1                |

Here, S0 represents the state where door is locked.

S1 represents the state where door is unlocked keyless.

S2 represents the state where door is unlocked manually.

Door lock output 0 reperesents that door is locked, and 1 represents door is unlocked.

FR represents face recognition, and MO represents manual override.
