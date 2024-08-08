# Instruction Set Design

## Instruction Set
### 0000xxxx : Basic Instructions
#### 0000 *
`push` : Push value that written at next byte to stack.

#### 0001
`pop` : Pop value from stack. 

#### 0010
`dup` : Copy top value on stack and push to stack.

#### 0011
`swap` : Replace top two values on stack.

#### 0100
`and` : Get top two values on stack, calculate the logical product and push to stack.

#### 0101
`or` : Get top two values on stack, calculate the logical sum and push to stack.

#### 0110
`xor` : Get top two values on stack, calculate the logical exclusive or and push to stack.

#### 0111
`not` : Get top value on stack, calculate the logical negation and push to stack.

#### 1000
`add` : Get top two values on stack, to add and push to stack.

#### 1001
`sub` : Get top two values on stack, to sub and push to stack.

#### 1010
`mul` : Get top two values on stack, to mul and push to stack.

#### 1011
`div` : Get top two values on stack, to div and push to stack.

#### 1100
`mod` : Get top two values on stack, to mod and push to stack.

#### 1101 *
`jmp` : Jump to address that written at next byte.

#### 1110 *
`jz` : Get top values on stack, if one isn't zero, jump to address that written at next byte.

#### 1111
`halt` : Stop to run program.

### 0001xxxx : Additional Instructions
#### 0000
`type` : Conversion top value on stack to type that written at next byte. Type is either next ones : u8、i8、bf8、char、bool.

#### 0001
`out` : Get top value on stack and print on default out.

#### 0010
`in` : Push value that from default input one char to top of stack.
