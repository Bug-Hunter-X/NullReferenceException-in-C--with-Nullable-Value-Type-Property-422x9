# NullReferenceException in C# with Nullable Value Type Property

This repository demonstrates a common C# error: a `NullReferenceException` occurring when attempting to access a member of a nullable value type property without explicitly checking for null.  The `Bug.cs` file contains the problematic code, while `BugSolution.cs` presents a corrected version.

## Problem

The `MyClass` class has a nullable `int` property (`MyProperty`). The `MyMethod` attempts to call `GetHashCode()` on this property, causing a `NullReferenceException` if `MyProperty` hasn't been assigned a value (it is null).

## Solution

The solution involves adding a null check before accessing `MyProperty`. This prevents the exception by handling the case where the property holds a null value.