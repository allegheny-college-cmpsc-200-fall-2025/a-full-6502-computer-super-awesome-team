# Report

| Verified by | Date |
|:------------|:-----|
|`TODO`|`TODO`|

## Speculation

> In your own words, describe what the 6522 tester code does.

It puts FF into the accumulator then it stores it at 0x6002. It then loads 55 into the accumulator and stores that value at 0x6000. Finally it load AA into the accumulator and stores it in 0x6000 replacing the value of 55 already stored there it then jumps back to 0x0005 and repeats from there.

> There are some addresses dedicated to using the interface. What are they and what do they seem to do?
> _HINT_: for this part, focus on the wiring of the _address bus lines_.

address line A0 - A3 are for using the interface as those depending on the values in the address tell the interface what to do with the data and how to represent it. It basically sets the mode the chip is in on other the PB pins should give back an input or an output if it should latch.

> Why is creating specific, separate addresses important to achieve this function?

So there aren't address conflicts between multiple parts if there is a consistent address that is to specifically to be used by the interface chip then it allows multiple devices to communicate with the chip efficiently and without confusion as long as they follow the established convention. 

> What is the value of the interface module (i.e. what does it _do_)?

It allows you to change the representation of data and to aid in communicating between 

