## To Do

- Route the DDR3 memory
- Do the Delay Matching for DDR3 memory
- check the validation of the pinout
- get the Correct values for the 100 Ohm differential pairs
- place the capacitors and resistors to the correct locations for the ddr3 chip
    - 4 capacitors were missing in original

- for next iteration
    - what to do with rot module interface
        - only keep one flash

SYS_PWROK_R - HPM_STBY_RST_N_R
SGPIO0_D0 U2 - SYS_PWRBTN_N_R V5
SGPIO0_DI W4 - SYS_PWROK_R p16
CHASI#_R Y3 - DBP_PREQ_N_R V2
SGPIO0_CLK W5 - DBP_PRDY_N_R W2
I2C[10]_SDA W6 - RST_PLTRST_BUF_N_R W1
SGPIO1_D0 Y6 - Spare1_R AA1
Spare0r y6 - spare1_r
SGPIO0_LD V7 - rot_cpu_rst_N_r
RSVD2 y7 - Chasi#_r
spare0_r y2 - i2c[11]_scl
irq_N_r ab1 - sgpio1_di
espi_io0 K17 - i2c[8]_sda
i2c[7]_sda E13 - espi_io1
i2c[7]_scl E13 - espi_io3 L16
i2c[6]_sda G13 - espi_reset_n
spi0_cs_n_r - espi_alert_n h18
spi0_clk_r - espi_cs0_n K18
uart0_scm_rx - espi_clk L18
espi_cs1_n - i2c[6]_clk
