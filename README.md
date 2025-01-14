# Rust Raw Pointer Vector Modification Bug

This repository demonstrates a common error in Rust when using raw pointers to modify vectors. Modifying a vector through a raw pointer after the vector's length or capacity has changed can lead to undefined behavior or a panic.  The example showcases this issue and provides a solution using safe Rust techniques.

## Bug Description
The `bug.rs` file contains code that attempts to modify a vector's element using a raw pointer. After obtaining the raw pointer, the vector's length or capacity could change, invalidating the pointer. This can result in unexpected program behavior or crashes.

## Solution
The `bugSolution.rs` file presents a safer solution using Rust's built-in methods to avoid the use of raw pointers whenever possible for safer memory management. 