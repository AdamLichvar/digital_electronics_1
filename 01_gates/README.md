# Lab 1: Adam Lichvár

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![Logic function](images/equations.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
    f_orig_o  <= (not(b_i) and a_i) or (c_i and not(b_i or not(a_i)));
    f_nand_o  <= not((not(not(b_i) and a_i)) and not(c_i and (not(b_i) and a_i)));
    f_nor_o   <= not(b_i or not(a_i)) or not(not(c_i) or (b_i or not(a_i)));
    
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

   ![image](https://user-images.githubusercontent.com/124684747/218748983-e22dcb8a-1d4f-429f-9292-d65e55c329dc.png)

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/peuS](https://www.edaplayground.com/x/peuS)
