# Error Handling Contract

This smart contract demonstrates the usage of `require()`, `assert()`, and `revert()` statements for error handling in Solidity.

## Contract Details

The `ErrorHandlingContract` contract allows you to perform the following actions:

- Check the usage of `require()` statement with the `checkRequire()` function.
- Get the current age value using the `getAge()` function.
- Check the usage of `revert()` statement with the `checkRevert()` function.
- Check the usage of `assert()` statement with the `checkOwner()` function.

## Error Handling Statements

### require()

The `require()` statement is used to validate conditions and revert the transaction if the condition is not met. It helps to enforce preconditions in the code.

- Function: `checkRequire(uint x)`
    - Parameters:
        - `x` (uint): Value to be added to the age.
    - Description: Checks if `x` is not equal to 0 using `require()`. If the condition is true, it adds `x` to the `age` variable.

### revert()

The `revert()` statement is used to explicitly revert the transaction with a custom error message. It is typically used to handle invalid conditions or unexpected behavior.

- Function: `checkRevert(uint x)`
    - Parameters:
        - `x` (uint): Value to be added to the age.
    - Description: Adds `x` to the `age` variable and checks if `x` is less than or equal to 0. If the condition is true, it reverts the transaction using `revert()`, providing a custom error message.

### assert()

The `assert()` statement is used to check for internal errors and should only be used in situations that should never occur. If an assert fails, it indicates a bug in the code.

- Function: `checkOwner()`
    - Description: Uses `assert()` to compare the `owner` variable with a specific address. If the comparison fails, it indicates an internal error.

