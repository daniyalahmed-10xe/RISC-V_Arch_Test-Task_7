# <center> RISC-V Arch Test </center>

## *<center> Implementation of Task 7 </center>*

#### Question Statement:

###### *Write a test to verify smepmp extension behaviour (Smepmp task)*

1. Pre-requisites:
	- Read RISCV privileged architecture spec for PMP.
	- Read about Smepmp extension.

2. Write an assembly test:
	- Start your test in M mode. 
	- Set mseccfg.MML.
	-  Add a rule with executable privileges that either is M-mode-only or a locked Shared-Region? what happens and why?
	- How can you solve the above problem?

#### Build & Run:

###### *Compile Assembly File to Elf:*

```shell
riscv64-unknown-elf-gcc -march=rv32imac_smepmp -mabi=ilp32 -nostdlib -T link.ld task7.S -o test.elf
```
###### *Create a Disassembly:*

```shell
riscv64-unknown-elf-objdump -D test.elf > test.disass
```

###### *Simulate on Spike & Generate Logfile:*

```shell
spike --isa=rv32imac_smepmp -l --log-commits test.elf 1> spike.out 2> spike.log
```

###### *Simulate on Sail & Generate Logfile:*

```shell
Sail DOES NOT Support SMEPMP...
```

#### Documentation:

###### *Source Code Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/task7.S
	</span>

###### *Log Files Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/spike.log
	</span>

###### *Report Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Report/RISC-V_Arch_Test_Task_7_Report.docx
	</span>

###### *Output Screenshots Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Screenshots
	</span>
