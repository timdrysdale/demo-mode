# demo-mode
Automated user that provides a "demo mode" for public experiments

Given a booking token (which must be limited to the exact set of experiments intended to do demo mode on) and sets demo commands to run, obtain a list of experiments, and randomly book them for short periods and play the demo commands.

For example, aim to have four of the motors in the set of 12 spinners working at any one time.

Tasks: step 6 radians. 

Spin at different voltages (open-source), step from 1 - 5V.

Implementation in go-lang would simplify running them in the background.

```
export DEMO_TOKEN=<login-token>
export DEMO_COUNT=4
export DEMO_TASKS=<contents of tasks.json>

./demo 
```

tasks.json:
```
{tasks:[{
  "name":"step",
  "duration":90,
  "commands":[{
    "wait":0.1,
    "cmd":"{<command>}"
  },{
  "wait":0.1,
  "cmd":"{<command>}"
  }
  ]},
 ... 
  
]}

```




