# Lab 2: Juraj Goryl

### 2-bit comparator

1. Karnaugh maps for other two functions of 2-bit comparator:

   Greater than, Less than:
   
![331440192_974232547269974_801738292463525452_n](https://user-images.githubusercontent.com/124798537/220186288-9c8c2212-699e-404a-a7e7-3ec0c1f83313.jpg)

   
2. Mark the largest possible implicants in the K-map and according to them, write the equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

  ![331573164_1198125484196461_8814147367019220640_n](https://user-images.githubusercontent.com/124798537/220188243-8b06a28c-951f-4514-814a-ca57551698c6.jpg)



### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: 13

p_stimulus : process
        begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0001"; 
        s_a <= "0011";
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination b=0001; a=0011 FAILED" severity error;
        
         -- Second test case
        s_b <= "0001"; 
        s_a <= "0011";
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '1') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination b=0001; a=0011 FAILED" severity error;
        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;

2. Link to your public EDA Playground example:

   https://www.edaplayground.com/x/BGZb
