# vending-machine
This project provides a Verilog implementation of a simple vending machine finite state machine (FSM). The vending machine accepts coins, keeps track of the current state based on the total value of the coins inserted, and dispenses an item when the required amount is reached.

Features
State Machine Implementation: The FSM handles four states (S0, S5, S10, S15), representing the total value of the coins inserted.
Coin Handling: Accepts two types of coins with values 1 and 2.
Output Signal: An output signal (nw_pa) indicates when the required amount (15) is reached, triggering the vending machine to dispense an item.
Reset Functionality: The machine can be reset to its initial state using a reset signal.
Test Bench: A comprehensive test bench (vending_machine_tb) is included to simulate and verify the functionality of the vending machine module.
Module Details
The vending machine module transitions through states based on the coin input:

S0: Initial state, transitions to S5 or S10 based on the coin inserted.
S5: Transitions to S10 or S15.
S10: Transitions to S15.
S15: Dispenses the item and resets to S0.
The test bench (vending_machine_tb) initializes the module, applies a sequence of coin inputs, and monitors the state transitions and output signal.

Usage
Clock Generation: A clock signal is generated with a period of 10 units.
Test Sequence: A sequence of coin inputs is applied to the vending machine, simulating various coin insertion scenarios.
Output Monitoring: The state and output signal are monitored and displayed during simulation.
