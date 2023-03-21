# Lab 6: Juraj Goryl

### Bidirectional counter

1. Listing of VHDL code of the completed process `p_cnt_up_down`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
        --------------------------------------------------------
    -- p_cnt_up_down:
    -- Clocked process with synchronous reset which implements
    -- n-bit up/down counter.
    --------------------------------------------------------
    p_cnt_up_down : process (clk) is
    begin
      if rising_edge(clk) then
        if (rst = '1') then           -- Synchronous reset
          sig_cnt <= (others => '0'); -- Clear all bits
        elsif (en = '1') then         -- Test if counter is enabled
          if (cnt_up = '1') then
              sig_cnt <= sig_cnt + 1;
          else
              sig_cnt <= sig_cnt - 1;
          end if;        
        end if;
      end if;
    end process p_cnt_up_down;
```

2. Screenshot with simulated time waveforms. Test: (a) reset, (b) counter direction, (c) enable. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![Snímka obrazovky 2023-03-21 184613](https://user-images.githubusercontent.com/124798537/226696980-8b76f448-7797-4622-9bde-21cb2fae6ae0.png)


### Two counters

1. Image of the top layer structure including both counters, ie a 4-bit bidirectional counter from *Part 4* and a 12-bit counter with a 10 ms time base from *Experiments on your own*. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!



  ![336583137_3570963673138087_8128021517350863751_n](https://user-images.githubusercontent.com/124798537/226718949-de14f502-0a24-45ab-a465-d933a8599055.jpg)

