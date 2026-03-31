# Problem 121 - Complex Number Class Implementation

## Summary

Successfully implemented a complete complex number class in C++ that passed all OJ test cases on the first submission with a perfect score of 100/100.

## Problem Requirements

Implement a complex number class (`sjtu::complex`) with the following functionality:

1. **Constructors**: Default, single parameter, double parameter, copy constructor
2. **Accessors**: `real()` and `imag()` methods returning references
3. **Unary Operators**: Negation (`-`) and conjugate (`~`)
4. **Binary Operators**: Addition, subtraction, multiplication, division
5. **Compound Assignment**: `+=`, `-=`, `*=`, `/=`
6. **Comparison**: Equality operator (`==`) with epsilon tolerance (1e-6)
7. **Type Conversion**: Explicit conversion to `bool`
8. **Output**: Stream operator with specific formatting (6 decimal places)
9. **Exception Handling**: `divided_by_zero` exception for division by zero

## Implementation Details

### Key Design Decisions

1. **Epsilon Comparison**: Used the provided `sign()` function with epsilon = 1e-6 for all floating-point comparisons
2. **Output Formatting**: Normalized values within epsilon to exactly 0.0 to avoid printing `-0.000000`
3. **Exception Handling**: Implemented `what()` method returning "complex divided by zero!"
4. **Complex Division**: Used the formula: (a+bi)/(c+di) = [(ac+bd) + (bc-ad)i] / (c²+d²)

### Test Results

**Submission ID**: 767216
**Status**: Accepted
**Score**: 100/100 (Perfect Score)
**Memory**: 4.29 MB
**Time**: 21 ms

All 10 test groups passed:
- Test 1: Constructors, assignment, accessors ✓
- Test 2: Unary operators (~ and -) ✓
- Test 3: Addition and subtraction ✓
- Test 4: Multiplication and division (no exceptions) ✓
- Test 5: Type conversion to bool ✓
- Test 6: Comparison operator ✓
- Test 7: Output function (relaxed precision) ✓
- Test 8: Output function (strict formatting) ✓
- Test 9: Arithmetic with exception handling ✓
- Test 10: Comprehensive stress test ✓

## Files

- `src.hpp`: Complete implementation of the complex class
- `test.cpp`: Local test file based on provided sample
- `submit_acmoj/acmoj_client.py`: Fixed submission script (added missing `submit_code` method)

## Submission History

- **Submission 1** (ID: 767216): **100/100** - All tests passed

## Conclusion

The implementation successfully handles all required functionality including:
- Proper construction and initialization
- All arithmetic operations with correct complex number mathematics
- Proper floating-point comparison with epsilon tolerance
- Correct output formatting with sign handling
- Exception handling for division by zero
- Type conversion operator

The code is efficient, readable, and adheres to the problem requirements.
