# Uncommon VHDL Counter Overflow Bug
This repository demonstrates a subtle bug in a VHDL counter implementation. The counter is designed to count from 0 to 15, but under specific conditions might not reset correctly, potentially resulting in unpredictable behavior.

## Bug Description
The `buggy_counter.vhdl` file contains a VHDL implementation of a counter.  The issue lies in the handling of the counter's reset condition and its interaction with the clock signal.  Under certain clock frequencies and reset timing scenarios the counter might fail to reset to 0 when `rst` is high, leading to incorrect values. 

## Solution
The `fixed_counter.vhdl` shows a corrected implementation of the counter.  The changes improve reset handling ensuring that the counter reliably resets to 0 when `rst` is high. 

## How to Reproduce
Simulate both the buggy and corrected counters using your preferred VHDL simulator.  Experiment with various clock frequencies and reset pulse widths to observe the difference in behavior.

## Note
This bug highlights the importance of carefully considering the timing aspects and interactions between signals in synchronous VHDL designs.  Properly handling reset signals in state machines and counters is crucial for reliable operation.
