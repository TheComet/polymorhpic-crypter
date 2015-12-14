////////////////////
//
//
//
// copyrly 2009
//
// permutative win32 executable crypter.
//
// generated files should always be unique.
//
// code that isn't mine is credited in the source if I knew who to credit.
//
// compile w/ MSVC, you will need to fuck with project settings to get it compile correctly.
// disable optimizations & exception handling.
//
// if u rip & not give creds i beat up ur mom, u 'nam? jk u.
////////////////////

+v1.0 (11/2008)
Pretty much just a recode of z0mbie's Real Permutation Engine since his shit fucks up a lot (A LOT), but its still an awesome idea so I tried to fix it.
*Added ETG engine (also by z0mbie) to add random junk code.
*Also ripped some of the mutatable instructions from RPME & Code Pervertor 2&3 for the Mutate() function & added a few new ones.

+v1.1 (01/2009)
*Added a shitload more instructions to Mutate() function. Results are more polymorphic now.

Stuff left to do:
-polymorphic loop generator.
-fix AddTrash() so that it sucks less.

== What do it does? ==
smiA?le will disassemble a block of code into a list of opcode information.
Using that list the engine can:

+add trash/junk code
+add random jmps to code
+mutate instructions

When reassembling, the instructions are written to a buffer in random(ish) offsets
and linked together with jmps.

This means you can take a block of code and (per)mutate and/or add junk until it is unrecognizable,
then write to a buffer (maybe already filled with random data ;D) to make code appear 100% different
and obfuscated. 