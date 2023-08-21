This repository contains all the assignments and information from the VLSI Physical Design for ASICs special topic taught at PES University, EC Campus, for ECE students, by [Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/) from [VLSI System Design](vlsisystemdesign.com)

This repo has been divided into various subfolders for different days of the coursework
Click on the links below to find the documents for each lab:
- [Lab 1](https://github.com/alfadelta10010/pes-asic-class/tree/main#day---1-lab-assignments)
- [Lab 2]() - WIP

## Set up instructions for the coursework
The software required is as follows:
- [RISC-V GNU Compiler Toolchain](https://github.com/riscv-collab/riscv-gnu-toolchain)
	- :warning: GCC-12 gives compiling issues for the proxy kernel, using GCC-8.3 solves this issue. You can download the pre-compiled toolchain from [here](https://static.dev.sifive.com/dev-tools/riscv64-unknown-elf-gcc-8.3.0-2019.08.0-x86_64-linux-ubuntu14.tar.gz)
- [Spike RISC-V ISA Simulator](https://github.com/riscv-software-src/riscv-isa-sim)
- [RISC-V Proxy Kernel and Boot loader](https://github.com/riscv-software-src/riscv-pk)


For a simple set up, you can use the set-up script provided by the instructor with the following commands:
```bash
git clone https://github.com/kunalg123/riscv_workshop_collaterals.git
cd riscv_workshop_collaterals
chmod +x run.sh
./run.sh
```

## Day - 1

![Screenshot from 2023-08-21 10-25-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0e706e45-29c5-4cfe-993b-8756421920e8)
![Screenshot from 2023-08-21 15-59-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b252c5fd-5e17-4064-ab6f-34c576c8f6e1)
![Screenshot from 2023-08-21 17-49-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2576945e-1897-4854-a6d5-199acac2d2e2)
![Screenshot from 2023-08-21 19-36-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b1897d87-972a-44b7-95c7-8ff267c7332f)

![Screenshot from 2023-08-21 20-09-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7a5d688c-aba8-452e-a104-b1aa31772d59)
![Screenshot from 2023-08-21 20-08-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/222d6c34-5cdb-447f-879c-07134e0c8acb)
![Screenshot from 2023-08-21 20-41-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0bf3d27a-dc8c-4aba-bc3f-443648e63a5b)
