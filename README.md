# SystemVerilog Protocol Verification Projects

Small SystemVerilog verification projects for **SPI, UART, and I²C** communication protocols.

These exercises were completed as course work while following **[Verification Series Part 2: Hands-On SystemVerilog Projects](https://www.udemy.com/course/systemverilog-for-verification-part-2-projects/)** on Udemy. The repository is mainly intended to document hands-on practice with class-based SystemVerilog verification concepts before moving to full UVM environments.

## Projects

- **SPI** — master/slave RTL with a simple procedural testbench and a class-based verification environment.
- **UART** — transmitter/receiver RTL with randomized TX/RX verification.
- **I²C** — master/slave RTL with constrained read/write transactions and a memory-based reference model in the scoreboard.

## Verification concepts practiced

Across the projects, the testbenches apply the main building blocks of a reusable SystemVerilog verification environment:

- transaction classes
- constrained-random stimulus and `randomize()`
- generator, driver, monitor, and scoreboard components
- mailboxes for transaction/data communication
- events for synchronization between verification components
- SystemVerilog interfaces and virtual interfaces
- concurrent execution using `fork...join`
- reset and stimulus tasks
- self-checking scoreboards
- simple reference modeling for read/write verification
- protocol-level monitoring of serial transfers
- VCD waveform generation for debug

These are **class-based SystemVerilog testbenches, not UVM**. The structure intentionally mirrors concepts that later map naturally to UVM components such as sequences, drivers, monitors, agents, and scoreboards.

## Repository structure

```text
.
├── spi
│   ├── rtl
│   │   └── spi_design.sv
│   └── tb
│       ├── spi_simple_tb.sv
│       └── spi_class_tb.sv
├── uart
│   ├── rtl
│   │   └── uart_design.sv
│   └── tb
│       └── uart_tb.sv
└── i2c
    ├── rtl
    │   └── i2c_design.sv
    └── tb
        └── i2c_tb.sv
```
