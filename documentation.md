# L+RatioLang documentation

## Types

There are only 3 data types in L+RatioLang:

+ boolean
+ integer/character
+ float

## Memory

The main memory is a stack you can use to store values.

You have also an array referred as `BT`, with an index referred as `BP` to access the values.

There are also 3 special registers: `RJ`, `RL`, `RS` which can contain, respectively, only boolean, integer and float values.

## Instructions

In this language there are two types of instructions: unary, and binary.  
Unary instructions have their distinct meaning on their own. You write it, it does its thing and eveyone is happy.  
On the other hand, binary instructions need to be combined with another binary instruction to form a meaningful expression.

A special character you will see a lot is the plus sign "+".  
It acts as a separator between instructions, so failing to write it in the right places will cause the program to not function properly or to fail completely.

Here you can see a little dictionary of all the instructions in L+RatioLang, divided into different categories.

### Functions

In L+RatioLang it is possible to create separated functions.  
The first function written in a program is considered the main function and is the first to be run.  
Different functions are identified by a number between 0 and n, where 0 is main, 1 the first function declared after main, and so on...

These instructions are used to work with functions.

+ **L**  
Declare a new function, which contains all the instructions until the next L

+ **rip bozo**  
Return to caller, if used while in the main function, exits the program

+ **common L**  
Call the function i, where i is the number contained in `RL`

### Registers

These instructions are used to interact with the registers.

+ **no job**  
Set `RJ` to `false`

+ **no life**  
Set `RL` to `0`

+ **no skills**  
Set `RS` to `0.0`

+ **no bitches**  
Set `BT[BP]` to `0`

+ **skill issue**  
Do `BP++`

+ **grammar issue**  
Do `BP--`

+ **what 0 pussy does to a mf**  
Set BT to `[]`, an empty array  

+ **hoes mad**  
Set something to be `BT.size()`  
e.g. *get a life + hoes mad* equals `RL = 0`

+ **get a job**  
Access `RJ`

+ **get a life**  
Access `RL`

+ **get real**  
Access `RS`

+ **get some bitches**  
Access `BT[BP]`

### Stack

These instructions are used to interact with the stack.

+ **go outside**  
push something on the stack

+ **touch grass**  
pop something from the stack, and saves it somewhere

### I/O

With these instructions you can read and write on the terminal.

+ **ok and?**  
read from the standard input and save it somewhere

+ **go tell Reddit**  
print something on the standard output

+ **screencapped your bio**  
print on the standard output information about the registers and the stack, useful for debugging

### Aritmetic/Logic

These instructions are used to perform arithmetic and logic operations.  
Some of these are basic operations, while the other exist for better usability, as they condense in one instruction many basic ones. 

+ **cringe**  
add 1 to something

+ **yikes**  
subtract 1 to something

+ **simp**  
add 5 to something

+ **furry**  
subtract 5 to something

+ **NFT owner**  
multiply something by 2

+ **you're white**  
divide something by 2

+ **problematic**  
elevate something to the power of 2

+ **irrelevant**  
perform square root of something

+ **get rekt**  
sets something to `0`

+ **reported**  
adds to `BT[BP]` the content of something

+ **cancelled**  
subtract from `BT[BP]` the content of something

+ **triggered**  
multiply something for `BT[BP]` and save in `BT[BP]`

+ **anime pfp**  
divide `BT[BP]` by something and save the quotient in `BT[BP]`

+ **you fell off**  
divide `BT[BP]` by something and save the remainder in `BT[BP]`

+ **no u**  
inverts the value of something

+ **minor spelling mistake**  
permorms bitwise AND between `BT[BP]` and something and saves result in `BT[BP]`

+ **opinion rejected**  
permorms bitwise OR between `BT[BP]` and something and saves result in `BT[BP]`

+ **fatherless behaviour**  
permorms bitwise XOR between `BT[BP]` and something and saves result in `BT[BP]`

### Flow control

With these instructions you can create loops and selections, mimicking for and if statements.

+ **kys**  
terminate the entire program

+ **cry about it**  
if `RL == 0` jump to next `log off`

+ **log off**  
exit point for `cry about it`

+ **stay mad**  
jump to previous `cope`

+ **cope**  
exit point for `stay mad`

+ **seethe**  
if `RJ == true` jump to next `mald`

+ **mald**  
exit point for `seethe`

+ **try again**  
repeat the previous non-control instruction

+ **\*you're**  
activate/deactivate the filter for bad-written instructions (with your instead of you're)

This is where we get to some funny stuff :)  

### Nopeops

These instructions are just something to make your code look longer, they do nothing at all.

+ **didn't ask**  
does nothing

+ **who asked**  
does also nothing

+ **any askers**  
does something, jk, does nothing

### Specops

These are instructions that didn't fall in any other category, as they do their own thing.  
They are pretty useful.

+ **ratio**  
add 1 to the ratio counter

+ **final ratio**  
set something to the ratio counter (max one per function, too powerful)

+ **who cares**  
set something to a random value

+ **xxx.xxx.xxx.yyy (IP address)**  
set something to a certain value, which is obtained this way:  
the first n x-digits are considered, starting from the least significant one, based on the yyy value, which can be:  
0-1 -> n = 3  
2 -> n = 6  
3 -> n = 9   
4 -> n = 3, number becomes negative   
5 -> n = 6, number becomes negative   
6 -> n = 9, number becomes negative  
7-255 -> n = 9

### Trollops

My favorites, these are instructions created only to disrupt and/or obfuscate the program they are written into.  
Ranging from mildly annoying to totally debilitating, once inserted into your code it will be difficult for anyone (including you) to understand what's going on afterwards.  
While silly, they can be used to create some complex weird code (I guess).

+ **pound sand**  
print "pounding sand\n" and sleep 1 second

+ **kick rocks**  
print "kicking rocks\n" and sleep an amount of second equal to the value in `RL`

+ **eat paper**  
print "eating paper\n", "mhh, tasty\n" and "nom nom nom\n" and also sleep for a random time (a while)

+ **i'm faster and stronger than you**  
add to every register and element of `BT` the value stored in `RL`

+ **you're going in my cringe compilation**  
invert the order of the elements in the stack

+ **not funny didn't laugh**  
invert the values of all the values in the registers and in `BT`

+ **you're allergic to sunlight**  
set to `1` any value everywhere

+ **terminally online**  
delete any value everywhere

+ **full time Discord mod**  
if `RJ == false` delete every value greater than 17, otherwise delete every value greater than 14 everywhere

+ **full time Reddit mod**  
set every value in registers and `BT` to `69` or `420`, accordingt to which is the closest one

+ **go off i guess**  
change the source code, inserting annoying trollops and nopeops