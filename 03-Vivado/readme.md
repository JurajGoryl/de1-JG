
# Lab 3: Juraj Goryl

### Three-bit wide 4-to-1 multiplexer

1. Listing of VHDL architecture from source file `mux_3bit_4to1.vhd`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of mux_3bit_4to1 is
begin

    f_o <= a_i when (sel = "00") else
       b_i when (sel = "01") else
       c_i when (sel = "10") else
       d_i; 


end architecture Behavioral;
```

2. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![vivado1](https://user-images.githubusercontent.com/124798537/221924284-3d0af004-0f23-47b5-8aca-4c513b153ad2.png)


3. Listing of pin assignments for the Nexys A7 board in `nexys-a7-50t.xdc`. **DO NOT list** the whole file, just your switch and LED settings.

```shell
##Switches
set_property -dict { PACKAGE_PIN J15   IOSTANDARD LVCMOS33 } [get_ports { a[0] }]; #IO_L24N_T3_RS0_15 Sch=sw[0] --input a LSB
set_property -dict { PACKAGE_PIN L16   IOSTANDARD LVCMOS33 } [get_ports { a[1] }]; #IO_L3N_T0_DQS_EMCCLK_14 Sch=sw[1] --input a
set_property -dict { PACKAGE_PIN M13   IOSTANDARD LVCMOS33 } [get_ports { a[2] }]; #IO_L6N_T0_D08_VREF_14 Sch=sw[2]  --input a MSB
set_property -dict { PACKAGE_PIN R15   IOSTANDARD LVCMOS33 } [get_ports { b[0] }]; #IO_L13N_T2_MRCC_14 Sch=sw[3]  --input b LSB
set_property -dict { PACKAGE_PIN R17   IOSTANDARD LVCMOS33 } [get_ports { b[1] }]; #IO_L12N_T1_MRCC_14 Sch=sw[4]  --input b
set_property -dict { PACKAGE_PIN T18   IOSTANDARD LVCMOS33 } [get_ports { b[2] }]; #IO_L7N_T1_D10_14 Sch=sw[5]  --input b MSB
set_property -dict { PACKAGE_PIN U18   IOSTANDARD LVCMOS33 } [get_ports { c[0] }]; #IO_L17N_T2_A13_D29_14 Sch=sw[6] --input c LSB
set_property -dict { PACKAGE_PIN R13   IOSTANDARD LVCMOS33 } [get_ports { c[1] }]; #IO_L5N_T0_D07_14 Sch=sw[7]  --input c
set_property -dict { PACKAGE_PIN T8    IOSTANDARD LVCMOS18 } [get_ports { c[2] }]; #IO_L24N_T3_34 Sch=sw[8]  --input c MSB
set_property -dict { PACKAGE_PIN U8    IOSTANDARD LVCMOS18 } [get_ports { d[0] }]; #IO_25_34 Sch=sw[9]  --input d LSB
set_property -dict { PACKAGE_PIN R16   IOSTANDARD LVCMOS33 } [get_ports { d[1] }]; #IO_L15P_T2_DQS_RDWR_B_14 Sch=sw[10]  --input d
set_property -dict { PACKAGE_PIN T13   IOSTANDARD LVCMOS33 } [get_ports { d[2] }]; #IO_L23P_T3_A03_D19_14 Sch=sw[11]  --input d MSB
set_property -dict { PACKAGE_PIN U11   IOSTANDARD LVCMOS33 } [get_ports { sel[1] }]; #IO_L19N_T3_A09_D25_VREF_14 Sch=sw[14] --select MSB
set_property -dict { PACKAGE_PIN V10   IOSTANDARD LVCMOS33 } [get_ports { sel[0] }]; #IO_L21P_T3_DQS_14 Sch=sw[15]  --select LSB

## LEDs
set_property -dict { PACKAGE_PIN H17   IOSTANDARD LVCMOS33 } [get_ports { out[0] }]; #IO_L18P_T2_A24_15 Sch=led[0] -- LSB of output
set_property -dict { PACKAGE_PIN K15   IOSTANDARD LVCMOS33 } [get_ports { out[1] }]; #IO_L24P_T3_RS1_15 Sch=led[1]
set_property -dict { PACKAGE_PIN J13   IOSTANDARD LVCMOS33 } [get_ports { out[2] }]; #IO_L17N_T2_A25_15 Sch=led[2] -- MSB of output
...
```
.
