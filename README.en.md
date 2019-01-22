# DSL4GC（Domain Specific Language for Game Control）

In [GameControllerizer](), game control information is expressed in an abstract format DSL4GC(Domain-specific Language for Game Control）. DSL4GC is expressed as JSON format, and is easy to read & edit. Appropriately changing this information and re-exporting it in Node-RED makes it possible to map it to inputs for games. 

## Example : StreetFighter2 "Hadouken (a.k.a Fireball)"
```Javascript
[
  {"dpad":[2], "dur":2}
  {"dpad":[3], "dur":2}  
  {"dpad":[6], "dur":2}
  {"dpad":[5], "btn":[0], "dur":2}
]
```

## Grammar
The operations of Gamepad/Mouse/Keyboard (= common game controllers) can be expressed in DSL4GC.
```Javascript
gc_sentence = Array[gc_gamepad_word]  |
              Array[gc_mouse_word]    |
              Array[gc_keyboard_word]
gc_gamaped_word = {c | c ∈ {"dpad","btn","stk0","stk1","cfg_input","dur"}}
gc_mouse_word = {c | c ∈ {"btn","mov","dur"}}
gc_keyboard_word = {c | c ∈ {"key","mod","dur"}}
```

## gc_gamepad_word
under construction...

## gc_mouse_word
under construction...

## gc_keyboard_word
under construction...
