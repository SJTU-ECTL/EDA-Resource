# Coding experience on circuit
1. When comparing the delays of two nodes, do not directly compare the delay values in float/double type.
For example, delay1 = 3.8000000000001, delay2 = 3.79999999999999, they are equal in reality.
However, if we directly compare their values in float/double type, they are inequal.
A solution is to compare "round(delay1 * 1000)" and "round(delay2 * 1000)" in C++.
