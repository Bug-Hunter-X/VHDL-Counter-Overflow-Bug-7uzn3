# VHDL Counter with Overflow Bug and Fix

This repository demonstrates a common bug in VHDL counters related to overflow handling and provides a corrected version.

## Bug Description
The `buggy_counter.vhd` file contains a VHDL counter that increments on each rising clock edge.  The counter is designed to have a range of 0 to 15. However, there is a subtle race condition issue or improper handling of the edge that may lead to incorrect behavior when the maximum count is reached.  The reset logic is also susceptible to issues if not properly synchronized with the clock.

## Bug Solution
The `fixed_counter.vhd` file provides a corrected version of the counter that addresses the described issues, ensuring proper reset and overflow handling.  Improved synchronization techniques between reset and clock signals were used.

## How to Reproduce
1. Compile and simulate `buggy_counter.vhd`. Observe the unexpected behavior under various clock speeds and reset scenarios.
2. Compile and simulate `fixed_counter.vhd` to see the corrected behavior.

## Technologies Used
* VHDL