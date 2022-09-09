# cfgpp-bf-interpreter
![Hello World](https://user-images.githubusercontent.com/69196954/189347944-aa019fe6-cdf1-408b-ac2b-f930f0473c74.gif)
Brainfuck interpreter written in [SAR]'s config+ language

## Usage

To run a brainfuck program:
* Place `bf-interpreter.cfg` in `Portal 2/portal2/cfg`. (or the equivalent folder for mods/[p2common])
* Ensure SAR is loaded. (`plugin_load sar`)
* Initialise the interpreter with `exec bf-interpreter` ingame.
* Run the program with `bf_exec <program>`. Note that user input syntax `,` is not yet supported and will be skipped over in execution.
Also note that programs greater than 247 characters long will be truncated, or 504 if the `bf_exec` is inside a `.cfg` that is `exec`'d.
This is unavoidable with current technology.

You can modify the speed at which the program is executed by running `svar_set __bf_delay <ticks>` where each tick is 1/60 of a second.
A delay of 0 will run the entire program immediately.

## Examples

Hello World:

      bf_exec ++++++++[>++++[>++>+++>+++>+<<<<-]>+>+>->>+[<]<-]>>.>---.+++++++..+++.>>.<-.<.+++.------.--------.>>+.>++.

[SAR]: https://sar.portal2.sr
[p2common]: https://www.youtube.com/watch?v=FmJ1OcKc7Ag
