# Architecture Design
This project can use two way. First as command. Another as library.
So divide to parts as command part and core part.
Command part that using core part is executable. Core part is as library.

## Core - Lib
This part is to decode asm and run one.

### VM
VM make by three parts.
Instuction memory, stack and program counter.

### Program Struct
Divide to understand structure easily.

#### instruction.rs
- Written motions each instructions.
- About basic and additional instructions.

#### io.rs
- Written motions each io.

#### stack.rs
- Written motions about stack.
- And motion of convert type instructions.

#### vm.rs
- Operate vm state, stack and program counter.

#### error.rs
- Written error of all things.

#### config.rs
- Written config of vm.

## Command - Exec
This part is to run asm as command.

### Program Struct
Divide to understand structure easily.

#### cli.rs
- Analysis the command line arguments.
- Providing a UI.
- Process about arguments and option at execute svvm command.

#### exec.rs
- Operat VM with call core method.

## Cargo.toml
``` toml
[package]
name = "svvm"
version = "0.1.0"
edition = "2021"
description = "A stack-based virtual machine"
license = "Apache-2.0"
authors = ["Q0tzly"]
repository = "https://github.com/Q0tzly/svvm/"
homepage = "https://q0tzly.com/"

[lib]
name = "svvm_core"
path = "src/lib.rs"

[[bin]]
name = "svvm_cmd"
path = "src/main.rs"

[dependencies]
```

## File Struct
```
/
|- Cargo.toml
|- docs
|  |- design
|  |  |- architecture.md
|  |  |- instruction_set.md
|  |  |- overview.md
|- LICENSE
|- README.md
|- src
|  |- main.rs
|  |- lib.rs
|  |- svvm_cmd
|  |  |- mod.rs
|  |  |- cli.rs
|  |  |- exec.rs
|  |- svvm_core
|  |  |- mod.rs
|  |  |- instruction.rs
|  |  |- io.rs
|  |  |- stack.rs
|  |  |- vm.rs
|  |  |- error.rs
|  |  |- config.rs
```
