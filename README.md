# VLSI Physical Design For ASIC
<br>

This course provides a comprehensive understanding of chip design using the RISC-V architecture. It covers key topics like design cycles, specifications, and SoC development. Students learn about analog IPs, mixed-signal flows, and gain hands-on experience with RISC-V-based SoC design. The curriculum also introduces process design kits, libraries, Verilog RTL design, synthesis, and the RTL-to-GDS flow for complete chip development. The course offers both theoretical insights and practical labs to equip students with essential skills in chip design.

## Skill Outcomes
1. Architectural Design
2. RTL Design/Behavioral Modeling
3. Floorplanning
4. Placement
5. CTS
6. Routing

## Skill Objectives:
• Prototype design ideas and enable low-volume chip design production with minimal
knowledge about tools
• Submit a silicon-ready datasheet and an IEEE format paper about their design
prototype.

## Installation
https://github.com/kunalg123/riscv_workshop_collaterals/blob/master/run.sh
1. Open Terminal<br>
2. Run the commands in run.sh file.


<details>
<summary>  WEEK -1 -> Day - 1</summary><br>



**C Program**

We wrote a C program for calculating the sum from 1 to n

![Screenshot from 2023-08-21 10-25-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0e706e45-29c5-4cfe-993b-8756421920e8)

![Screenshot from 2023-08-21 15-59-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b252c5fd-5e17-4064-ab6f-34c576c8f6e1)


**RISCV GCC Compiler and Dissemble**


> Using the riscv gcc compiler, we compiled the C program.

> riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum11.o sum11.c

> Using ls -ltr sum1ton.c, we can check that the object file is created.

> To get the dissembled ALP code for the C program,

> riscv64-unknown-elf-objdump -d sum11.o | less .

> In order to view the main section, type /main


When we use -Ofast optimisation, we can see that the number of instructions have been reduced to 12


![Screenshot from 2023-08-21 21-36-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f6a42c13-58a3-4533-b9d1-467973a4d250)

**Integer Number Representation**

**Unsigned Numbers**


    Unsigned numbers, also known as non-negative numbers, are numerical values that represent magnitudes without indicating direction or sign.
    Range: [0, (2^n)-1 ]


**Signed Numbers**


    Signed numbers are numerical values that can represent both positive and negative magnitudes, along with zero.
    Range : Positive : [0 , 2^(n-1)-1] Negative : [-1 to 2^(n-1)]


**Labwork**


We wrote a C program that shows the maximum and minimum values of 64bit unsigned numbers.




![Screenshot from 2023-08-21 17-49-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2576945e-1897-4854-a6d5-199acac2d2e2)

![Screenshot from 2023-08-21 19-36-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b1897d87-972a-44b7-95c7-8ff267c7332f)

![Screenshot from 2023-08-21 20-09-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7a5d688c-aba8-452e-a104-b1aa31772d59)

![Screenshot from 2023-08-21 20-08-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/222d6c34-5cdb-447f-879c-07134e0c8acb)

![Screenshot from 2023-08-21 20-41-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0bf3d27a-dc8c-4aba-bc3f-443648e63a5b)

![Screenshot from 2023-08-21 21-52-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/38ac1e72-dd0e-41ee-bda8-c9719081d8df)

</details>


<details>
    

<summary> WEEK 1 -> Day - 2</summary>
# Using ABI (Application Binary Interface) function calls in lab work typically involves working with low-level programming languages like Assembly or understanding how different programming languages interact at the binary level. Here's a general outline of what lab work involving ABI function calls might entail:

## Lab Objective: To understand and demonstrate the usage of ABI function calls in programming.

Steps:

    Select a Programming Language: Choose a programming language in which you'll demonstrate ABI function calls. Common choices include Assembly, C, or C++.

    Write Simple Functions: Create a few simple functions in the chosen language. These functions will serve as examples for demonstrating ABI function calls. Make sure to include functions with parameters and return values.

    1. Compile Code: Compile the code into object files or binaries, depending on the chosen language.

    2. View Binary Code: Use tools like objdump or disassemblers to view the binary code of the compiled program. This will help you understand how the function calls are translated into machine instructions.

    3. Create a Calling Program: Write a calling program that calls the functions you defined earlier. This calling program will demonstrate how function calls are made according to the ABI.

    4. Parameter Passing: Experiment with different parameter passing methods based on the ABI. For example, observe how arguments are passed using registers or the stack.

    5. Return Values: Explore how return values are handled. Understand which registers or memory locations are used to store the return values.

    6. Calling Conventions: Study the specific calling conventions for your chosen language and platform. Different ABIs have different rules for parameter passing, register usage, and stack management.

    7. Debugging and Analysis: Use debugging tools to step through the calling program and observe the behavior of function calls. This will help you understand how the ABI dictates the interaction between the caller and the callee.

    8. Documentation: Document your observations and findings regarding how ABI function calls work in the chosen programming language. Include explanations of parameter passing, return values, and any specific conventions you've explored.

    9. Presentation: If required, present your lab work to the class, highlighting the importance of ABI in enabling interoperability between different software components.

### By working through these steps, you'll gain a deeper understanding of how ABI function calls facilitate communication between different parts of a program, even when they are written in different programming languages or compiled separately. This lab work is valuable for students studying computer science, computer engineering, or any field involving low-level programming and system interactions.


![Screenshot from 2023-08-21 23-17-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/31109d79-59d1-49f7-99f9-195dff6f9ac5)


![Screenshot from 2023-08-21 23-18-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6bdfa28b-a795-47c3-9b7f-2074bc6352ac)

  

![Screenshot from 2023-08-21 23-51-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/440ffc79-a475-4788-9ddf-44c5717aa617)

![Screenshot from 2023-08-21 23-37-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/22b7e404-7a85-42d0-8070-895e49741350)

![Screenshot from 2023-08-21 23-46-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ad818a35-a8d5-4203-8a25-fc61e516a371)

![Screenshot from 2023-08-21 23-48-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a66470a2-bedd-4a35-a724-75f931256f88)


![Screenshot from 2023-08-21 23-49-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a6b19848-7257-4978-9a42-d04aacb31a0c)

![Screenshot from 2023-08-21 23-50-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9f75cbc5-453f-490d-8fc3-6240be0bf2ac)

</details>





<details>
  <summary>
       WEEK-2 -> Day - 1
  </summary>



# Introduction to Yosys and Logic Synthesis

### Yosys is an open-source tool that performs logic synthesis, a crucial step in digital circuit design. It transforms high-level hardware descriptions (in languages like Verilog) into optimized gate-level representations. This conversion involves hierarchy handling, parsing, optimization, technology mapping, and logic restructuring. Yosys aids in creating efficient designs for implementation on FPGAs and ASICs. It also offers formal verification to ensure correctness. Overall, Yosys simplifies the process of turning abstract hardware concepts into practical circuit implementations.
<br>

![Screenshot from 2023-08-26 10-07-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/910449b9-2b4c-4520-98c4-d4f34562c0ac)

![Screenshot from 2023-08-26 10-07-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f892ed77-b4b1-4194-b0c3-79478a0c655b)
## Synthesis
### Synthesis is the process of transforming a high-level hardware description (often written in a hardware description language like Verilog or VHDL) into a lower-level representation consisting of gates, flip-flops, and other logic elements. This process optimizes the design for factors such as performance, area, and power, making it suitable for implementation on hardware platforms like FPGAs or ASICs
* In the context of digital design and hardware description languages (HDLs) like Verilog, the ".v" extension is used to indicate that a file contains Verilog source code. Verilog is a popular HDL used for describing the behavior and structure of digital circuits. The ".v" extension is a common convention to help identify Verilog files.

* In Yosys, the read_verilog command is used to read and parse Verilog files. Verilog is a hardware description language (HDL) commonly used for describing digital circuits and systems. The read_verilog command allows you to import Verilog source files into Yosys for further processing, such as synthesis, analysis, optimization, and verification.

* In Yosys, the read_liberty command is used to import and read Liberty format files. Liberty files provide information about the timing, power, and characteristics of standard cells in a digital library. Yosys uses this data during logic synthesis to optimize designs based on the properties of the cells in the target library, ensuring better timing, power, and efficiency in the synthesized circuits.

 * In Yosys, the write_verilog command is used to generate and export a Verilog representation of the synthesized design or internal data structures. This command outputs the synthesized design, including any optimizations or transformations, into a Verilog file that can be further analyzed, simulated, or used in downstream stages of the digital design flow.


![Screenshot from 2023-08-26 10-07-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/28be91b1-0194-455e-a575-73df676277fa)

* A netlist is a digital circuit's blueprint represented as interconnected components and their connections. It describes how basic elements like logic gates and flip-flops are wired together to create a functioning circuit. Netlists are used to guide physical design and implementation processes, bridging the gap between high-level design and actual hardware layout.

* A test bench is a set of simulation or verification code used to test and validate the functionality of a digital circuit or system. It provides input signals to the design under test, monitors its outputs, and checks if the behavior matches expected results. Test benches are crucial for verifying that a design works correctly before it's implemented in hardware.

* iverilog is an open-source simulator and compiler for the Verilog hardware description language (HDL). It allows you to compile and simulate Verilog code, enabling you to test and verify the behavior of digital circuits through simulation. iverilog is widely used by digital designers and engineers to validate their designs before actual hardware implementation.

* A VCD (Value Change Dump) file is a standard format used to store and represent simulation data from digital design and verification tools. It captures changes in signal values over time during a simulation run. VCD files are commonly used to visualize and analyze the behavior of digital circuits, making them essential for debugging and verifying the correctness of designs through waveform viewers and analysis tools.

* GTKWave is an open-source waveform viewer that allows you to visualize and analyze simulation results stored in formats like VCD (Value Change Dump) files. It provides a graphical representation of signal waveforms over time, helping engineers and designers analyze the behavior of digital circuits during simulation. GTKWave is widely used in the field of digital design and verification for debugging and understanding the operation of digital systems.

![Screenshot from 2023-08-27 21-49-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/97c35d54-e1fc-41b1-9f2d-9aa7188388b7)

![Screenshot from 2023-08-27 21-51-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7044dc3c-0257-4bd8-bf21-474eec09491b)

![Screenshot from 2023-08-27 21-51-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d9318470-5c15-4407-8aa8-99490d79ad50)

![Screenshot from 2023-08-27 21-51-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8162c3f3-6547-457d-a23a-514b1fdd73bc)


![Screenshot from 2023-08-27 21-55-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8155fe82-dfd3-47a8-93d8-c27f8f24e02c)

![Screenshot from 2023-08-26 22-13-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/af9b00aa-5fb0-4f62-8a2b-f35363b9634d)

![Screenshot from 2023-08-27 19-51-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7fccb57b-09c6-49b5-ab0b-48d6762b35fa)

![Screenshot from 2023-08-27 21-55-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/eb39c73d-ff5d-4050-919c-513645e0d2b8)

![Screenshot from 2023-08-27 21-07-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/df509fb6-f4be-44e7-b002-436fe033094b)

</details>







<details>
    
<summary> WEEK-2 -> Day - 2 </summary>

# Introduction to dot lib


![Screenshot from 2023-08-28 10-20-38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/76ff4fbc-1645-4772-a7aa-d4080cd8b2a9)

![Screenshot from 2023-08-28 14-15-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/87767a9e-3acf-4707-9d4f-24aac76ebb2b)

![Screenshot from 2023-08-28 14-54-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/04958aee-c402-4caf-86d7-778cee3e063a)


![Screenshot from 2023-08-28 14-58-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/daa6776a-d34d-4afb-93a4-f35dac3a892c)

![Screenshot from 2023-08-28 15-22-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5d583965-2f7e-4526-bd6c-b27536efda05)

# Hierarachical vs Flat Synthesis

![Screenshot from 2023-08-28 16-13-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a8373588-7b71-4a83-a70b-d486a2349560)

![Screenshot from 2023-08-28 16-18-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4fd6d5f3-d281-497a-a792-0b9afe2fe88c)

![Screenshot from 2023-08-28 17-25-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a52423e4-9e8a-4e7c-81aa-15c63d93cf0c)

![Screenshot from 2023-08-28 17-25-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2606ea61-450e-40be-8cee-de1641c525e3)

![Screenshot from 2023-08-29 05-45-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/110e7082-0c7b-4e6a-8dd6-eab652c2e79d)

![Screenshot from 2023-08-29 05-57-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8cd09d23-ca2f-4a70-b87f-c44b9d8f9884)

![Screenshot from 2023-08-29 05-57-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1083c270-20d2-4532-9af4-97c163de0822)




![Screenshot from 2023-08-29 05-58-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/413a2dc7-9e70-4b1a-9f67-75e6a0e37d84)


![Screenshot from 2023-08-29 06-05-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1c05f4d9-0a54-4fdf-a03c-50eed7f7fe3d)

![Screenshot from 2023-08-29 06-06-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/29163ae5-02d6-4f38-9a13-85574d178f42)

![Screenshot from 2023-08-29 06-10-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0e416a0a-8a0a-4fd7-8711-8d737ec2467f)

![Screenshot from 2023-08-29 06-15-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/dfa6aabd-aa7b-4a1f-b8f3-64ca48f925f4)


![Screenshot from 2023-08-29 06-14-45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8a2c9553-ece2-4d21-a867-6a751574079c)

![Screenshot from 2023-08-29 06-16-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fa1b0fe9-f606-44eb-b5cf-75d9bffb703c)

![Screenshot from 2023-08-29 06-16-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4035e930-698a-447b-b8fc-19449bac4b1d)


# Various Flop Code Styles and Optimization 
- Why Flops and Flop Coding Styles
- Lab flop synthesis simulations
- Intersyning Optimisations


![Screenshot from 2023-08-29 20-28-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a125e493-e3f0-4357-9a39-b9a499a1be36)

![Screenshot from 2023-08-29 20-46-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f7eafad2-ab3c-4f1e-9ef8-cc525759f584)

![Screenshot from 2023-08-29 20-46-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/aea1f55f-8184-45fd-bcee-67088444542f)

![Screenshot from 2023-08-29 20-47-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/249a220d-6ebf-4e6b-9394-a4e6bb700f95)

![Screenshot from 2023-08-29 20-47-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/efba0892-c648-4638-9f45-64e0dc7386c9)

![Screenshot from 2023-08-29 21-00-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bffb49c4-c091-460a-a149-efa3f680b0a2)

![Screenshot from 2023-08-29 21-01-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e6325a21-4ccf-4332-bdc7-5b26066d06c5)


![Screenshot from 2023-08-29 21-01-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1e8915b0-c7f8-4ff6-8d13-324c3c003557)


![Screenshot from 2023-08-29 21-01-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/be448b4d-f714-437b-b774-6004af1b8f64)


![Screenshot from 2023-08-29 22-19-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8c447adb-95a0-4ce1-9bf1-14092cf4ab7b)


![Screenshot from 2023-08-29 22-19-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/197b07f1-6d1f-4b40-a5f1-ec6e12d0c268)

![Screenshot from 2023-08-29 22-39-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b9cbe95a-065c-43f9-942a-1855517c0874)

![Screenshot from 2023-08-29 22-39-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5eea6750-534a-4c9e-90e1-5e2b6b4ac0fb)

![Screenshot from 2023-08-29 22-40-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2f5afbdb-e3d2-44cd-8acb-842cad8ad8cf)

![Screenshot from 2023-08-29 22-40-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5286c0af-38f8-4679-af23-b6d30b5a1cc3)

![Screenshot from 2023-08-29 22-40-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/54000e0e-407f-4306-9222-3cd4c9874cac)

![Screenshot from 2023-08-29 23-02-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d712b0b5-4760-4756-a815-35458a8675de)

![Screenshot from 2023-08-29 23-03-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/853ef49d-eda5-452a-9e43-aef64c49f26e)

![Screenshot from 2023-08-29 23-04-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/adf24b33-6f10-475e-8b68-80c943f1930a)

![Screenshot from 2023-08-29 23-04-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7ab01d42-e70e-4a48-a4a6-ecf431985ee6)

![Screenshot from 2023-08-29 23-05-24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8cbdb5bd-b048-4360-8699-8d66d55f468b)

![Screenshot from 2023-08-29 23-05-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9a6563e6-99e4-4002-961a-47fde29b02ba)

![Screenshot from 2023-08-29 23-06-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/12035d21-1ac8-458d-820f-691ce2d0ae03)

![Screenshot from 2023-08-29 23-06-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b15d9a16-596f-42d2-94c7-ff3dc124bfd9)

![Screenshot from 2023-08-29 23-13-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ff15d816-f58b-4ef0-ad6a-6493d06f0161)

![Screenshot from 2023-08-29 23-27-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/78ca3026-4b26-4b76-bf6f-b00316b31bd6)

![Screenshot from 2023-08-29 23-27-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a72e99a2-8065-4ad9-aa2e-58b505f0cf49)

![Screenshot from 2023-08-29 23-37-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/43665d07-1921-4fdb-a69e-1a3030174dc9)

![Screenshot from 2023-08-29 23-37-33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1d74bd7e-2f4e-4fa6-b9a8-b65ed6c1a316)

![Screenshot from 2023-08-29 23-37-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b89e0c04-30b5-4907-8462-66fe472433cf)
![Screenshot from 2023-08-29 23-39-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/28dc5d70-bc97-4458-b085-2c17a5a41bd4)

![Screenshot from 2023-08-29 23-39-24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3322a0d5-23cf-43ac-8c42-7cbe1054126c)


</details>



















<details>
    
<summary> WEEK-2 -> Day - 3 </summary>

# Combinational and Sequetial Optimisations

- Introduction to Optimisation




    1. Combinational Logic Optimisation
  
![Screenshot from 2023-08-30 22-23-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/36701a6c-1fff-4fd8-84a4-2a308b01182c)
![Screenshot from 2023-08-30 22-24-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/123ba7a7-8481-4613-ba5c-a561b0e249bc)
![Screenshot from 2023-08-30 22-24-33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2e0c04ba-070c-4302-b4e5-7f418fcc2faa)

    2. Sequential Logic Optimisation
    
![Screenshot from 2023-08-30 22-24-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c16ca43b-7966-4762-89df-daf591bcc6a7)
![Screenshot from 2023-08-30 22-25-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c9c69dad-c98b-424b-8fac-75dbdb6bb566)






- Combinational Logic Optimisation Lab Implemention

## Verliog code for otp_check
![Screenshot from 2023-08-30 23-51-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d5ef414c-ac4b-4dda-8ae8-f88770c49624)
## Pratical implemention of otp_check
![Screenshot from 2023-08-30 23-26-03](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/62302c34-cd6f-442a-a07d-b3f7d106d237)
## Using Yosys implemention of otp_check
![Screenshot from 2023-08-30 23-38-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/61403cb8-83c9-47ee-9718-693f65cd3717)
![Screenshot from 2023-08-30 23-39-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1f32d4a0-49ba-4879-8b33-394479e0bd26)
![Screenshot from 2023-08-30 23-39-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9fbabebf-9a6d-4c5f-8741-955a3cd166d2)
![Screenshot from 2023-08-30 23-39-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/dc1da4cf-2081-4707-a0fc-3e0fc4293578)
![Screenshot from 2023-08-30 23-40-11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8ad8ce12-416b-41d4-b62b-2a58dfba0ecf)


## Verliog code for otp_check2
![Screenshot from 2023-08-30 23-51-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/33461fc0-8855-4f5d-8795-44968bd32e19)
## Pratical implemention of otp_check2
 ![Screenshot from 2023-08-30 23-26-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a8b64528-6eeb-4395-8fbe-b847f6e5047d)
## Using Yosys implemention of otp_check2
![Screenshot from 2023-08-30 23-44-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8641d680-629b-4082-bca2-81a9c6d5e325)
![Screenshot from 2023-08-30 23-44-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/110d0c6e-4228-4d70-aa4a-8e230641473c)
![Screenshot from 2023-08-30 23-45-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cb3af423-594d-4dad-a976-ae5ba37e71ee)
![Screenshot from 2023-08-30 23-45-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ea4dcc67-5d26-4bae-aa70-04e314baa7db)

## Verliog code for otp_check3
![Screenshot from 2023-08-30 23-52-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/70a54cd1-5295-4cde-8e7d-7a714804b654)

## Pratical implemention of otp_check3
![Screenshot from 2023-08-30 23-53-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6bf3d3bf-3793-4c83-807c-64cd492358c7)

## Using Yosys implemention of otp_check3
![Screenshot from 2023-08-30 23-56-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/66b2e77c-5fa5-4ec5-ab14-f429e1d3d2d3)
![Screenshot from 2023-08-30 23-56-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7880a756-d8b1-47ac-af30-9fbe845c9e84)
![Screenshot from 2023-08-30 23-56-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b4ebb9b3-6f05-4a5e-836d-7ce72270df32)
![Screenshot from 2023-08-30 23-57-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/095bbaa5-8b5a-4722-b7c7-a74af0c6de29)





## Verliog code for otp_check4
![Screenshot from 2023-08-30 23-53-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8e66fccf-508b-4141-b015-86997c248190)

## Using Yosys implemention of otp_check4
![Screenshot from 2023-08-31 00-01-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7bf80901-261b-4eda-9c74-b995d1f7831d)
![Screenshot from 2023-08-31 00-02-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/657a537a-ad3b-4269-a627-bbb869ff16dc)
![Screenshot from 2023-08-31 00-02-22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/283b4350-6eaa-42d4-ad85-bff003e8e76e)
![Screenshot from 2023-08-31 00-02-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9a0c75b4-5091-4d6c-8dd4-0b3880056a38)

## Verliog code for multiple_module_opt
![Screenshot from 2023-08-31 00-13-22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b490d3ef-dc09-4751-a40d-dcc5ab7bbfd0)



## Using Yosys implemention of multiple_module_opt
![Screenshot from 2023-08-31 00-11-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3f2646d6-0e96-40d9-a3b0-2568e3028c78)
![Screenshot from 2023-08-31 00-11-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1668d98a-77fb-4026-b225-a020d97e0eb6)
![Screenshot from 2023-08-31 00-12-05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/690a848b-2bd4-4381-9866-9be862b9ca23)
![Screenshot from 2023-08-31 00-12-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/88e86d23-a31a-4094-95a3-724361a39e06)

## Verliog code for multiple_module_opt2
![Screenshot from 2023-08-31 00-14-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0b715e9a-d175-46ca-bf53-deea84ea8c77)

## Using Yosys implemention of multiple_module_opt2
![Screenshot from 2023-08-31 00-16-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/958c1d49-1018-4171-b47e-f49b1d8aec8a)
![Screenshot from 2023-08-31 00-17-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a1a4c100-d571-4db9-80d3-0debaf495eee)
![Screenshot from 2023-08-31 00-17-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/370cf605-6623-443c-89d9-b156460f1c77)
![Screenshot from 2023-08-31 00-17-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/311e363f-b1ee-4a8d-a925-aa06ade80708)












- Sequential Logic Optimisation

- Sequential Optimization for Unused Outputs





</details>



<details>
    
<summary> WEEK-2 -> Day - 4 </summary>
# GLS,blocking vs non-blocking and synthesis-Simulation mismatch

- GLS,Synthesis-Simulation mismatch and Blocking/Non-blocking Statements
    1. GLS Conepts and Flow using iverliog
    2. Synthesis Simulation Mismatch
    3. Blocking and non-blocking statements in verilog
    4. caveats with blocking statements
- Labs on GLS and Synthesis-Simulatuion Mismatch

- Labs on synth-sim mismatch for blocking statement

</details>



