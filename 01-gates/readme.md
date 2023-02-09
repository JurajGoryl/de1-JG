# Lab 1: Juraj Goryl

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![329864082_721626092739810_5335380770398649465_n](https://user-images.githubusercontent.com/124798537/217839636-e972b832-66ca-4136-a3b8-a6b17fc88302.jpg)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
    f_orig_o <= (not(b_i) and a_i) or
                (c_i and not(b_i or not(a_i)));
    f_nand_o <= not(not(((not(b_i) and (a_i)))) and not(((c_i) and((not(b_i) and (a_i))))));
    f_nor_o  <= not((b_i) or not(a_i)) or not(not(c_i) or ((b_i) or not(a_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

   | **c** | **b** |**a** | **f_ORIG** | **f_(N)AND** | **f_(N)OR** |
   | :-: | :-: | :-: | :-: | :-: | :-: |
   | 0 | 0 | 0 | 0 | 0 | 0 |
   | 0 | 0 | 1 | 1 | 1 | 1 |
   | 0 | 1 | 0 | 0 | 0 | 0 |
   | 0 | 1 | 1 | 0 | 0 | 0 |
   | 1 | 0 | 0 | 0 | 0 | 0 |
   | 1 | 0 | 1 | 1 | 1 | 1 |
   | 1 | 1 | 0 | 0 | 0 | 0 |
   | 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![Snímka obrazovky 2023-02-09 152609](https://user-images.githubusercontent.com/124798537/217840427-0dd05d03-8b5f-4f98-a9d6-14d285ec27ea.png)


2. Link to your public EDA Playground example:

   https://edaplayground.com/x/F8Ug
