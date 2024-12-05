# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: counter overflow. The `counter.vhdl` file contains a simple counter that increments when an enable signal is high. However, it lacks a check for the upper bound of the counter, leading to potential overflow when the counter reaches its maximum value. 

The `counter_solution.vhdl` file provides a corrected version of the code that addresses the overflow issue by checking for the upper limit before incrementing the counter.

## Bug Description
The bug lies in the lack of overflow checking in the counter's increment logic. When the counter reaches 15, the next increment will result in an overflow, causing unpredictable behavior.  This is a subtle error that can be missed during code review.

## Solution
The solution involves adding a check to ensure that the counter does not exceed its maximum value (15). If the counter reaches 15, it should wrap around to 0 or remain at 15, depending on the desired behavior.