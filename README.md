# radare2 development docs

Some personal notes I sometimes write down while making r2.

## Index
[PJ API](#PJ-API)

[r2r and tests](#Tests)

## PJ API

#### What's PJ API?

PJ API is the API radare2 uses to print the JSON output of many of the existing commands.

#### tl;dr

You would start with a:  `PJ * pj = pj_new (); ` to create a new PJ instance, then choose whether you want an object or an array, `pj_o ()` or   `pj_a ()` , or both and use the required method according to your need: character array, float, to suit your needs

#### Location
`libr/include/r_util/pj.h` has information about all the PJ functions. There are different functions for each data type, choose the right one.

#### Commits 

[PJ API in `isj`](https://github.com/radareorg/radare2/commit/0d701a3b7972ced7eb450504ffbdffbe8273c303)

[PJ API in `oj`](https://github.com/radareorg/radare2/commit/4a406503c476348c7d958ddf7bd2e87f98e43cd1)

## Tests
radare2 has a test suite to properly test whether the command has been implemented properly. You can find the README about that in [~/test](https://github.com/radareorg/radare2/tree/master/test).

To run an individual test:

`$ r2r -i $path_to_the_file`
For example: 
`$ r2r -i db/cmd/cmd_open `