VLSI Physical Design For ASIC
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
<br>



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


  ## Verliog code for dff_const1
![Screenshot from 2023-08-31 22-03-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a864479d-1071-4f15-9aeb-700ad8407daf)

## GTKwave form for dff_const1
![Screenshot from 2023-08-31 20-50-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8d2ae770-3e06-4c96-98c0-3829f9fe5445)
![Screenshot from 2023-08-31 20-50-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e3c76d34-e33c-4518-9292-e49b1342f854)


  ## Using Yosys implemention of dff_const1
![Screenshot from 2023-08-31 20-56-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/44149bcc-830c-451d-8819-78f539b69c00)

![Screenshot from 2023-08-31 20-56-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a35e05c3-8b2b-4c64-8841-79b8b4cb9987)
![Screenshot from 2023-08-31 20-56-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b7649d5b-efc6-4a26-9a7b-ec08aadcfdc0)
![Screenshot from 2023-08-31 20-57-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/63e61d25-a325-4ae8-8f53-43a35de73b6c)
![Screenshot from 2023-08-31 20-57-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/34d45be4-feec-46b8-bdd1-b50f8024f805)




  ## Verliog code for dff_const2
![Screenshot from 2023-08-31 22-03-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9415b54b-eca1-47b1-81bb-80e9529483a3)


## GTKwave form for dff_const2
![Screenshot from 2023-08-31 20-53-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0b1a29aa-6dce-43ac-b25d-6ea75ce318c8)
![Screenshot from 2023-08-31 20-53-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e4e9aa7e-025f-44e0-ab42-9fa4ca4d7e0c)


  ## Using Yosys implemention of dff_const2
![Screenshot from 2023-08-31 20-59-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e5bd29f0-dac6-4dcb-98ed-b4d24bdef7ef)
![Screenshot from 2023-08-31 20-59-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b165d953-03a9-4512-bb9c-3a650cbe287c)
![Screenshot from 2023-08-31 20-59-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ed216e9b-19b3-4f02-81a5-ca551a8d6dea)
![Screenshot from 2023-08-31 21-00-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9bd15cab-1768-4dee-a0e8-31704e45ad6e)





  ## Verliog code for dff_const3
![Screenshot from 2023-08-31 22-03-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8f072550-2e72-45e6-be8f-d711974232bf)


## GTKwave form for dff_const3
![Screenshot from 2023-09-01 00-43-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3907e109-5132-43b6-aec5-952c3828d61b)


  ## Using Yosys implemention of dff_const3
![Screenshot from 2023-08-31 22-08-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bcdd1210-575b-489d-9d8b-3ce10db965f7)
![Screenshot from 2023-08-31 22-08-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/97008c1b-3991-4534-8584-f1d4dbf9ad01)

![Screenshot from 2023-08-31 22-08-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4e44f80f-dc65-47f3-a8c9-0c645a7817c2)

![Screenshot from 2023-08-31 22-08-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/186e6134-d34e-4aa1-9d0f-015df65dbe16)

![Screenshot from 2023-08-31 22-08-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/75398475-7ee8-4c99-b99b-b3a7a8b2f925)






  ## Verliog code for dff_const4
![Screenshot from 2023-08-31 22-04-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f14ad186-bb0d-488b-9f5c-08fda5cb335b)



## GTKwave form for dff_const4
![Screenshot from 2023-09-01 00-44-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7fd4435c-5d58-40d6-843e-12b97d1ac86d)



  ## Using Yosys implemention of dff_const4
![Screenshot from 2023-08-31 22-11-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bce9c131-be04-447d-9b0a-cc9eb05929e3)

![Screenshot from 2023-08-31 22-11-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9e31ea79-a061-4411-afd8-095a5dd36891)

![Screenshot from 2023-08-31 22-11-51](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b8699b80-af54-44fe-8ad3-c26531a3ce18)


![Screenshot from 2023-08-31 22-12-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/156736d6-b0c1-4a29-973d-5e388cf25ca7)



  ## Verliog code for dff_const5
![Screenshot from 2023-08-31 22-05-45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c4a69cdb-de61-4c8d-b7ef-630963f7ba65)



## GTKwave form for dff_const5
![Screenshot from 2023-09-01 00-47-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4092a9d7-2b0c-4997-95a9-2f54d5ff5c25)

![Screenshot from 2023-09-01 00-47-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a5e4be43-53a8-4720-ac6e-91ae2004a2f6)


  ## Using Yosys implemention of dff_const5
![Screenshot from 2023-08-31 22-13-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b682947f-61c8-4608-9a14-49c8bae51b66)

![Screenshot from 2023-08-31 22-13-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/52d057b9-27e5-4192-adfc-ab9893de8d7d)
![Screenshot from 2023-08-31 22-14-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/744d5ae0-f3fb-4139-ae74-dd59c784b398)

![Screenshot from 2023-08-31 22-14-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fb995170-7887-4aa7-9c6e-67fed35c3228)
![Screenshot from 2023-08-31 22-14-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6f2ef0e5-ca1b-433f-83d6-b38e324b666c)


- Sequential Optimization for Unused Outputs
  ## Verliog code for counter_opt
![Screenshot from 2023-09-01 09-29-03](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8a40f6cd-8451-421e-a61d-0920330b675a)

  
## Pratical implemention of counter_opt
![Screenshot from 2023-09-01 09-51-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/387c39ec-2a56-4321-a5c4-06049acc70b5)

 
 
 ## Using Yosys implemention of counter_opt
![Screenshot from 2023-09-01 09-30-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/31b78ba2-9cbe-4101-9c22-03f9b480163b)
![Screenshot from 2023-09-01 09-30-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e9d20f76-ae8c-47ca-8d29-6a0abd447332)
![Screenshot from 2023-09-01 09-31-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4761bc9e-c58c-4c73-a508-b380961bc8bb)
![Screenshot from 2023-09-01 09-31-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a3d3f29b-dfbf-4d90-83ac-50015834793f)




 
 ## Verliog code for counter_opt2
![Screenshot from 2023-09-01 09-49-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f523d213-ccf3-4e6c-a523-27f03f9ec03b)

## Pratical implemention of counter_opt2
![Screenshot from 2023-09-01 09-22-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f78a376e-11a6-4944-b25c-06ffa05b2b23)
![Screenshot from 2023-09-01 09-26-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f6686619-2611-4b06-aa98-be9e9fdce94e)

 
 
 ## Using Yosys implemention of counter_opt2
![Screenshot from 2023-09-01 09-41-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5bf2cc47-43ec-4f89-83fb-d0b23babc398)
![Screenshot from 2023-09-01 09-41-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3dab84d8-e89b-4723-a5ee-b5827c2579c1)

![Screenshot from 2023-09-01 09-41-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3d7ba26b-db3b-427d-97db-351a2d6a6488)
![Screenshot from 2023-09-01 09-41-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fe9b6f70-f655-462c-b79e-c0c5ff368242)
![Screenshot from 2023-09-01 09-42-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/715d17e5-7059-414f-ba3d-c2c492a07dbe)


</details>



<details>
    
<summary> WEEK-2 -> Day - 4 </summary>
# GLS,blocking vs non-blocking and synthesis-Simulation mismatch

- GLS,Synthesis-Simulation mismatch and Blocking/Non-blocking Statements
  
    1. GLS Conepts and Flow using iverliog
   ![Screenshot from 2023-09-02 11-07-09](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c0abbb14-6826-403d-a246-7821b470205d)
![Screenshot from 2023-09-02 11-10-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b70c16b7-dc23-4aa1-bc05-9ad5ba6bb9fd)

![Screenshot from 2023-09-02 11-18-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8b7c981e-5cc8-4b90-a1e8-7d9337976057)


    2. Synthesis Simulation Mismatch

![Screenshot from 2023-09-02 11-19-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cc5ec975-e0ab-4953-b123-5c68e2cf8095)
![Screenshot from 2023-09-02 11-27-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b9700152-f724-4788-be0a-5cb7b2c977c3)

    
    3. Blocking and non-blocking statements in verilog
    
![Screenshot from 2023-09-02 11-30-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f2b82778-2cf8-497d-8eaf-f767c2362831)

![Screenshot from 2023-09-02 11-41-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/867101ca-38cd-4862-a1f1-932ce5e26a38)

![Screenshot from 2023-09-02 11-43-45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/57e98768-d4ab-47f0-bd17-6ddd6c42f57b)

    4. caveats with blocking statements
![Screenshot from 2023-09-02 11-50-33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/74d216cc-1637-4ecc-a20f-77ea28799f9a)


- Labs on GLS and Synthesis-Simulatuion Mismatch
  
  ![Screenshot from 2023-09-03 13-06-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/abcd5229-cd93-4b6d-ba39-1366e9e1b1e9)

![Screenshot from 2023-09-03 12-52-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5a48f82c-e270-4bed-90cc-d34efaed6b70)

![Screenshot from 2023-09-03 14-17-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0f239e86-2052-4270-a9f0-c6fe1c70ad3d)
![Screenshot from 2023-09-03 12-52-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/53ee19d2-3146-4241-8149-45caf84ff72b)

![Screenshot from 2023-09-03 14-18-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0fab181d-5fc6-45c3-99fa-951212943505)
![Screenshot from 2023-09-03 14-19-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7d6b57d7-b34c-4d9f-bfe0-884032f76c56)
![Screenshot from 2023-09-03 13-01-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9addf27f-df01-48c5-aaf5-e5be9dee49ed)
 ### By GLS
 ![Screenshot from 2023-09-03 14-39-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/29eed1aa-bf52-4866-93f7-f59daa4f2636)
![Screenshot from 2023-09-03 14-42-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8202e911-ec46-43b7-9513-730f72d6a0ba)

![Screenshot from 2023-09-03 14-37-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fd5ed7cd-a5e5-4daf-b5f8-3f9196470142)

![Screenshot from 2023-09-03 14-38-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a072fba4-0773-4d45-bbde-7dc27d839d2b)

![Screenshot from 2023-09-03 14-39-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b766e6e6-3d33-4c1e-a9a8-9a331643d45f)
![Screenshot from 2023-09-03 14-39-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a7c85960-b7e8-4f87-9796-f3f212f97fdd)

![Screenshot from 2023-09-03 13-01-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3959665f-f55c-4d3a-a94d-b2ece9afec30)

- Labs on synth-sim mismatch for blocking statement

![Screenshot from 2023-09-03 16-51-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/23f56216-ed93-4706-945b-5c579807fb69)

![Screenshot from 2023-09-03 17-13-09](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a5e91d1b-e446-4daa-b35d-7cd2f08c5719)
![Screenshot from 2023-09-03 17-16-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b0ce27f5-e98a-445f-b6c7-f64749f05290)

![Screenshot from 2023-09-03 17-14-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a62de006-3bf0-4345-a742-590b2f61882b)



![Screenshot from 2023-09-03 17-24-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ac3582f8-5538-424f-9b35-b08504a29a58)

![Screenshot from 2023-09-03 17-34-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/76cd284d-0f7f-46c4-a130-d8642d3730c1)


![Screenshot from 2023-09-03 17-31-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/14d2570b-cdcf-43d3-a54d-e48fdb661616)
![Screenshot from 2023-09-03 17-32-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/dddcc749-2a80-4d46-9bce-58661c858737)

</details>





<details>
    
<summary> WEEK-3 -> Day - 1 </summary>

# Inception of open-source EDA,Openlane and sky130 PDK

1. How to talk to computers

- ### Introduction to QFN-48 Package, chip, pads, core, die and IPs
![Screenshot from 2023-09-09 06-02-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/695b807a-7c14-477f-b8b7-a8670f9b223c)
![Screenshot from 2023-09-09 06-02-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/faa79ff0-b5fd-44f1-9a21-99d3f6612064)
![Screenshot from 2023-09-09 06-07-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/742e86b7-2dce-46b0-83eb-384c006be7c7)
- ### Introduction to RISC-V 
![Screenshot from 2023-09-09 06-15-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/142bf0d9-c983-4620-b9cd-3f8d8e0607f0)
- ### From Software Applications to Hardware
![Screenshot from 2023-09-09 06-23-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f974b6c9-427b-4f43-944e-da9699ead689)
![Screenshot from 2023-09-09 06-26-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d802184a-2295-4295-81a1-f79b7e9ba0e6)
![Screenshot from 2023-09-09 06-30-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cdd950e9-6753-4ea1-8bcc-fee87249efb4)
![Screenshot from 2023-09-09 06-30-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8cdbb1c6-58af-496a-86e2-7e2200f86ccf)
![Screenshot from 2023-09-09 06-32-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/094a034a-0e0e-4b05-b99c-9552eb722f55)
![Screenshot from 2023-09-09 06-33-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ea956daf-6700-4e58-9b79-fb8ddfc07757)




      
2. SoC design and OpenLANE
   
- ### Introduction to all components of open-source digital asic design
![Screenshot from 2023-09-09 07-30-03](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2a1a0387-6815-4d47-9b28-f324726ba4e4)  
![Screenshot from 2023-09-09 07-30-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b2ce9eef-6a3c-4358-b504-d7b54ce921a8)
![Screenshot from 2023-09-09 06-43-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bb816d18-16bf-44de-a2f9-7ecbc7b24c03)
![Screenshot from 2023-09-09 06-45-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2d8de8b3-1cea-408b-95f0-27dbdcd5ede1)
![Screenshot from 2023-09-09 06-46-09](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6d7165ed-10e0-49d1-9c83-ae9aff5e4cdd)
![Screenshot from 2023-09-09 06-47-05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c816f90f-96de-4738-a5bf-499f7bd9d9e8)
![Screenshot from 2023-09-09 07-34-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3b39394e-e429-4a70-9b45-b0f72980b228)
![Screenshot from 2023-09-09 06-49-03](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e54fcea7-42be-480a-a5d6-ffd8eec77cc7)
![Screenshot from 2023-09-09 07-34-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e4f18abc-577b-4d5f-b0f6-0aae6aa5eccb)
![Screenshot from 2023-09-09 07-34-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/53018ea5-a708-4c76-ac49-c5bac92afaeb)
- ### Simplified RTL2GDS flow
![Screenshot from 2023-09-09 06-50-24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ad4bef26-0f88-4170-8d06-19360aad0b7c)
![Screenshot from 2023-09-09 06-54-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/23483640-fa8e-4dc1-80b7-e65a3069d7e3)
![Screenshot from 2023-09-09 06-55-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/927c00cb-7b48-4565-b3b7-3282d3337a68)
![Screenshot from 2023-09-09 06-58-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a19983cf-39c5-46dd-b646-62aeeeddaabb)
![Screenshot from 2023-09-09 06-57-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/03237927-fcc2-4cbe-ab00-9c1c2065dafe)
![Screenshot from 2023-09-09 06-58-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/61eb09a3-b04e-4baf-8dd1-11641bc32fa6)
![Screenshot from 2023-09-09 06-59-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/db4f7e9b-28dd-4ac3-84e5-b24d0153f1e4)
![Screenshot from 2023-09-09 07-00-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2f75fbe5-f039-4fb8-bcc1-d90967c24cb9)
![Screenshot from 2023-09-09 07-01-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3947b886-8f2b-4902-b27a-e03052bf1a56)
![Screenshot from 2023-09-09 07-02-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c23008a0-a1c0-4e67-a558-741c2283f4a9)
![Screenshot from 2023-09-09 07-03-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/af26b1b7-c8ed-4d63-b2b7-cb1d3da1ac23)
![Screenshot from 2023-09-09 07-04-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ad0a4962-74f4-4b95-a67c-b7ecb85bedc8)
- ### Introduction to OpenLANE and Strive chipsets

![Screenshot from 2023-09-09 09-56-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/74a6c5ef-984b-43cc-b52a-c81a6f822f74)
![Screenshot from 2023-09-09 09-57-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0019dce8-b9b6-4102-b53a-e186d8041eb2)
![Screenshot from 2023-09-09 10-13-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/76bead52-2eb4-44ed-b9fe-765bf1a0147f)
![Screenshot from 2023-09-09 10-16-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7e1e519e-cf03-466c-9edd-7c34e74717be)
![Screenshot from 2023-09-09 10-19-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7baaa97b-3c29-4950-bbe1-622432301339)


- ### Introduction to OpenLANE detailed ASIC design flow 
![Screenshot from 2023-09-09 10-23-05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/aac57c8c-303b-461a-bac2-9f5319aee1b6)
![Screenshot from 2023-09-09 10-23-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ff0b2373-df5a-4580-92b7-a88c487dd07a)
![Screenshot from 2023-09-09 10-24-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/efb4bc96-c5e0-47b0-85f2-6d1b7409de76)

![Screenshot from 2023-09-09 10-25-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d7d6efb8-0152-4252-9c27-9c5d74a5f61d)
![Screenshot from 2023-09-09 10-27-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/53a62565-a0a0-4df6-a37c-494ee9908c4f)
![Screenshot from 2023-09-09 10-28-38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1ea49299-82b4-4bf6-9fda-1ff3cd8f0d23)
![Screenshot from 2023-09-09 10-29-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2050278f-83ac-4e0b-826d-8a2a5eaeecaf)
![Screenshot from 2023-09-09 10-30-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/89db9c39-d2b6-474e-b8e4-8fa3855468f6)
![Screenshot from 2023-09-09 10-31-22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/050c1721-ef33-440b-9be8-ae29f4d4cae6)
![Screenshot from 2023-09-09 10-33-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e5ffc34f-cf90-4454-9985-86e730600d53)
![Screenshot from 2023-09-09 10-34-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/267af47b-d5f1-4f84-a7ee-c15f2c54630f)
![Screenshot from 2023-09-09 10-34-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/590931b7-1c65-430e-8158-13641ce78cb8)
![Screenshot from 2023-09-09 10-35-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e6d17ffb-1504-402c-9cf8-ab1de64043bf)
![Screenshot from 2023-09-09 10-36-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/08a6587a-b2f8-4b07-9214-a61df3cf02ad)






3. Get familiar to open-source EDA tools

   - OpenLANE Directory structure in detail
    ![VirtualBox_PES_physical_design_09_09_2023_12_41_45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0b10a680-5228-48d9-9c51-54482cfe4434)
![VirtualBox_PES_physical_design_09_09_2023_12_42_38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/334584a0-022f-4a19-86b6-bede9905a115)
![VirtualBox_PES_physical_design_09_09_2023_12_56_32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4efe581e-d324-415e-8f3a-cd3879239809)


   - Design Preparation Step

![VirtualBox_PES_physical_design_09_09_2023_13_13_16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3f1994c9-cece-40fe-b0c1-1f3b18aa5a9d)

![VirtualBox_PES_physical_design_09_09_2023_13_17_33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3addbae5-2509-4506-bd7c-3f361e7c3b15)

![VirtualBox_PES_physical_design_09_09_2023_13_09_55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/754e2dac-b1af-48cf-a580-787128371e9e)

![VirtualBox_PES_physical_design_09_09_2023_13_22_05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d432b3aa-0935-406c-a4d2-85ec2caaa87b)



     
   - Review files after design prep and run synthesis

![VirtualBox_PES_physical_design_09_09_2023_14_18_21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d33d509e-261d-4c96-85a0-1049b5bb76b7)
![VirtualBox_PES_physical_design_09_09_2023_14_18_43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/271d6aa4-e4a6-4299-af29-01e1d059b52b)
![VirtualBox_PES_physical_design_09_09_2023_14_23_49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6aee9d70-bbd8-4a1b-be5d-892a381df571)
![VirtualBox_PES_physical_design_09_09_2023_14_24_16 (copy)](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5b26da08-c581-4992-9717-f30bd0052508)
![VirtualBox_PES_physical_design_09_09_2023_14_34_27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d8ccba8e-9346-4f0e-bc95-4404eca91147)

   - OpenLANE Project Git Link Description

     
   - Steps to characterize synthesis results
     


</details>



<details>
<summary> WEEK-3 -> Day - 2 </summary>
    
# Good floorplan vs bad floorplan and introduction to library cells 

## 1. Chip Floor planning considerations
- ### Utilization factor and aspect ratio
![Screenshot from 2023-09-09 17-05-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a6b04b88-19c9-4bf4-b50c-c66b82a97f83)
![Screenshot from 2023-09-09 17-08-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f4b2e552-ccd6-4f1a-85f2-fff1659e7bea)
![Screenshot from 2023-09-09 17-08-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7006410d-f0fb-451c-9e88-575f2f5549c5)
![Screenshot from 2023-09-09 17-09-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/355baa94-6ad0-4501-9c35-7406f43fc1c2)
![Screenshot from 2023-09-09 17-10-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3f8e1c2e-4089-45f8-b1b5-186b0969adfb)
![Screenshot from 2023-09-09 17-11-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4ccebca1-f5c7-453a-bb0d-f1f77a676b02)
![Screenshot from 2023-09-09 17-15-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f4dbf488-9808-4a73-8042-e39d7434fe19)
![Screenshot from 2023-09-09 17-16-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5d032cf3-79aa-4d43-bb8a-d4bf65d3b120)
![Screenshot from 2023-09-09 17-17-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8286b4c6-787d-45bf-9f4e-0c4645b41283)
![Screenshot from 2023-09-09 17-27-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/84fdc0b9-e7ff-4a33-8825-d36e936d17a0)
- ### Concept of pre-placed cells
![Screenshot from 2023-09-09 17-27-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7326d5c8-4fcd-4d4e-aa60-79a64b6e743a)
![Screenshot from 2023-09-09 17-30-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d9596c35-dbbe-4d5f-97ac-8eb9e9575863)
![Screenshot from 2023-09-09 17-31-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/32c864ba-de42-48e9-a35f-a18d2ab41d46)
![Screenshot from 2023-09-09 17-31-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/40f12baa-f590-4a57-af24-245145946b65)
![Screenshot from 2023-09-09 17-36-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/28b67020-01c1-4833-8414-b51dd858455c)
- ### De-coupling capacitors
![Screenshot from 2023-09-09 17-49-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/90ddb5ea-0705-495a-943a-4f18faee94f3)
![Screenshot from 2023-09-09 17-50-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5eda99f0-31fa-4d80-9115-0db3f2de834f)
![Screenshot from 2023-09-09 17-50-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/06ea0d8d-99df-4e5d-8193-17986d795e83)
![Screenshot from 2023-09-09 17-54-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b8e21e2c-c497-4d18-8a71-230a85b37d91)
![Screenshot from 2023-09-09 17-54-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/460807a7-f1a0-4879-b7b7-c78a5d267d60)
![Screenshot from 2023-09-09 17-56-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f27dab67-a579-4fcb-8d84-415ecb7faac3)
![Screenshot from 2023-09-09 17-58-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/61a310d2-eb5a-4776-93d6-e69daad3e199) 
- ### Power planning
![Screenshot from 2023-09-09 18-01-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bde6a89f-1814-446e-8e0d-b83767c44984)
![Screenshot from 2023-09-09 18-07-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6284c266-648b-4272-8afc-436430428fc9)
![Screenshot from 2023-09-09 18-10-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/56bcf7fd-b5d7-48d2-bb63-123729a22b1a)
![Screenshot from 2023-09-09 20-47-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/66909f0f-3d0a-457d-b68a-0a9a9c447df7)
![Screenshot from 2023-09-09 20-48-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ef5d3088-e56d-461f-9ac1-5e27a1c6daf6)
![Screenshot from 2023-09-09 21-23-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/68aa57e7-b8ed-42ed-8b1c-fb7a2f7f6bd6)
![Screenshot from 2023-09-09 21-25-22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a8b71c86-3ca3-49c0-8d93-2fda9b9cce5d)
![Screenshot from 2023-09-09 21-26-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e987d3ec-9eed-4493-bb47-71e9ec8296ce)
![Screenshot from 2023-09-09 21-27-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a1534d99-c024-44bb-a8e8-18657d145dff)
- ### Pin placement and logical cell placement blockage
![Screenshot from 2023-09-09 21-52-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b7c1eeb7-e8f1-4c56-a616-954913a75a36)
![Screenshot from 2023-09-09 21-54-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f058f48b-2b68-4c92-ae8d-df14e73d3ab9)
![Screenshot from 2023-09-09 21-57-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5f297541-ed9d-447a-9f63-7d4f450e2cfa)
![Screenshot from 2023-09-09 21-58-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7b74b091-194c-4bed-b54a-72f58ed7d8ab)
![Screenshot from 2023-09-09 21-59-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/033bf491-3c59-4064-ad19-f870b581956b)
![Screenshot from 2023-09-09 22-01-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/554ff639-61a1-428c-b87c-98b2e3b61551)
![Screenshot from 2023-09-09 22-01-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/07b99ebf-23c1-408b-ad4c-97d8b694e428)
![Screenshot from 2023-09-09 22-04-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4c724b84-67fb-46a7-9615-ac38955722c4)
![Screenshot from 2023-09-09 22-04-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/14f1fa11-c58b-49c9-bf7e-6aee538776bb)
- ### Steps to run floorplan using OpenLANE

![VirtualBox_PES_physical_design_09_09_2023_14_34_27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d341fc94-3035-4493-9df8-092253095dda)
![VirtualBox_PES_physical_design_10_09_2023_13_10_29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c57a8377-e68a-40d3-b46f-263386ff547f)


![VirtualBox_PES_physical_design_10_09_2023_13_04_34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6a3b2c7e-e697-418b-b004-0127074357c4)

![VirtualBox_PES_physical_design_10_09_2023_13_05_12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2c38e324-dd85-4332-b058-bf5be2e8fc0b)

![VirtualBox_PES_physical_design_10_09_2023_13_06_45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ccb7e80a-6883-40c7-b85d-7408fa747519)

![VirtualBox_PES_physical_design_10_09_2023_13_08_50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e94998c3-9433-4eb4-b913-e8fed09c326e)
![VirtualBox_PES_physical_design_10_09_2023_13_15_11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/98eb1e12-c61c-469e-bc79-1c591c06fd5d)


      
- ### Review floorplan files and steps to view floorplan
![VirtualBox_PES_physical_design_10_09_2023_13_23_34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bbb4cb8c-1171-4124-8d61-9c27bc37c7cb)
![VirtualBox_PES_physical_design_10_09_2023_13_29_05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/abef7228-c8e3-4e7e-b357-2ade0d8e56c6)

![VirtualBox_PES_physical_design_10_09_2023_13_35_11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e9c9fb49-4cc0-4243-9c90-9e34fc83cfa3)




- ### Review floorplan layout in Magic
![VirtualBox_PES_physical_design_10_09_2023_13_35_11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/dea63558-5ff9-4ed0-85a9-99c21a3a66fb)
![VirtualBox_PES_physical_design_10_09_2023_13_36_34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/397d08d6-2710-4850-b98d-da5ccef10d60)
![VirtualBox_PES_physical_design_10_09_2023_13_43_39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/739be89f-2952-4325-94be-9bfd106c3386)
![VirtualBox_PES_physical_design_10_09_2023_13_50_58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/910e6c03-2c5d-4858-9e70-2b522c9a8352)
![VirtualBox_PES_physical_design_10_09_2023_13_52_52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/58a7e660-6df5-45d7-88a9-63eaa4bb1fe6)


    
      
## 2. Library Binding and Placement
- ### Netlist binding and initial place design
![Screenshot from 2023-09-15 05-29-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fc6cd943-ee51-42f8-bb30-f0a2f146c9af)
![Screenshot from 2023-09-15 05-30-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c883e3a5-23b5-4b2e-962d-a2a9ef384644)
![Screenshot from 2023-09-15 05-33-11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/88b34d62-ded2-44db-998c-da2713212bee)
![Screenshot from 2023-09-15 05-34-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/25ab9bba-7878-486a-91fa-721b21adfb99)
![Screenshot from 2023-09-15 05-38-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6f697327-3547-49b8-85a3-43e3d269d18d)      
- ### Optimize placement using estimated wire-length and capacitance
![Screenshot from 2023-09-15 05-43-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1c23eece-63d6-4ab0-a604-31878b7b02c9)
![Screenshot from 2023-09-15 05-44-24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f86aec2b-4541-4527-9601-c05d845a6174)
![Screenshot from 2023-09-15 05-51-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/30a4081b-fd70-4001-8c58-c7fbf7d72408)
![Screenshot from 2023-09-15 05-52-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f7ab42c0-60f7-484f-a5af-0002fabf5055)     
- ### Final placement optimization
![Screenshot from 2023-09-15 06-00-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/dfcdeb5d-8a21-4bc1-bcee-b1d875dcda8e)
![Screenshot from 2023-09-15 06-10-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/50806cc0-6418-4469-89f8-eaeb2f42dff3)
![Screenshot from 2023-09-15 06-13-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b7084e70-2073-4e59-a2fd-3ef8a0776fa9)      
- ### Need for libraries and characterization
![Screenshot from 2023-09-16 07-08-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ebfba563-6498-4421-b724-b93183c27de2)
![Screenshot from 2023-09-16 07-09-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c16d9c4d-fd10-4a60-9783-f06e6fe78923)
![Screenshot from 2023-09-16 07-09-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/57b04d20-a130-4edc-b73d-e1ca6ca9f8f8)
![Screenshot from 2023-09-16 07-10-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e2f09f14-49d7-4e5d-8f37-ab4299a2e374)
![Screenshot from 2023-09-16 07-12-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/384369d2-42a3-4250-903e-ecfd69d5f7b9)
![Screenshot from 2023-09-16 07-13-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/da6db991-9a6c-4303-ab5e-d35c529e5edb)
![Screenshot from 2023-09-16 07-15-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b85e6b61-4d40-4219-9d4f-adb2708e53df)
![Screenshot from 2023-09-16 07-16-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/443bd744-d3d1-4176-a525-c9b24864ca76)
- ### Congestion aware placement using RePlAce
![VirtualBox_PES_physical_design_16_09_2023_10_19_27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ef889f7b-4591-47fc-b88a-3ff8d9f8a3f9)
![VirtualBox_PES_physical_design_16_09_2023_10_36_26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/712f4acd-4bcd-4287-b47b-4e7d4dc1003c)
![VirtualBox_PES_physical_design_16_09_2023_10_44_22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c9d5e5ad-7b7f-4423-807b-91d8c33266de)
![VirtualBox_PES_physical_design_16_09_2023_10_44_38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8b100217-ea8b-4355-a1db-e0fd8dfee340)
## 3. Cell design and characterization flows
- ### Inputs for cell design flow
![Screenshot from 2023-09-16 16-18-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ed0d99d4-0412-4e50-ae97-34e5d5513039)
![Screenshot from 2023-09-16 16-21-11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ea6caf18-caed-42a2-8794-059480556b91)
![Screenshot from 2023-09-16 16-37-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f88a418a-eb13-4ba4-80af-6a1774b8670c)
![Screenshot from 2023-09-16 16-42-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/22cdf526-6a87-4001-93b7-0c961ccedc90)
![Screenshot from 2023-09-16 16-44-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/40bcaecf-9419-49a0-81a4-e3bba85d9936)      
- ### Circuit design step
![Screenshot from 2023-09-16 16-48-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4f1e8cb1-82f5-4401-873b-a0b60ad9ab13)
![Screenshot from 2023-09-16 16-50-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7a1d96ab-86a0-4c54-a247-b07c211951df)
![Screenshot from 2023-09-16 16-50-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/115028a8-d6b4-42e5-bbe2-7f3b26386193)
![Screenshot from 2023-09-16 16-51-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bf6f777f-1f69-4cdd-a81e-360f1da71677)
![Screenshot from 2023-09-16 16-52-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1c1cabcd-7e15-4bd1-a8da-5d341db01e42)
![Screenshot from 2023-09-16 16-55-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cc72af8e-25a1-4010-87e4-da5b3996ef56)
- ### Layout design step
![Screenshot from 2023-09-16 17-04-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3c7a2ffd-31bc-400e-8060-846c3e9e36f8)
![Screenshot from 2023-09-16 17-05-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4c216dde-065c-4334-b220-dba3ac97a28c)
![Screenshot from 2023-09-16 17-05-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/45a800fb-d061-4f44-b7f5-f9a94340f1d0)
![Screenshot from 2023-09-16 17-07-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/08180396-e554-4d6f-ab77-b90766064760)
![Screenshot from 2023-09-16 17-08-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/860f7aab-7f90-4fd6-b214-60285edc26dc)
![Screenshot from 2023-09-16 17-09-24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/988a4747-ea42-486e-841a-fece00d6a2fe)      
- ### Typical characterization flow
![Screenshot from 2023-09-16 17-12-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/503e8d02-899e-4b98-9ccd-ae824ecac670)
![Screenshot from 2023-09-16 17-12-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2eb7aed4-dd89-496c-ad0f-7ca14bdb2809)
![Screenshot from 2023-09-16 17-15-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4599d25d-a8d4-4899-9352-aa5154cfc46f)
![Screenshot from 2023-09-16 17-16-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/adf857a4-7e8f-4be0-81f8-ac9109c9ff60)
![Screenshot from 2023-09-16 17-16-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/196ea324-a945-4312-8529-c65703879bd6)
![Screenshot from 2023-09-16 17-16-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d700337c-5670-4243-97ef-7c2c4534522f)
![Screenshot from 2023-09-16 17-17-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/496c3864-f17a-47ca-8f62-12dc51fa89eb)
![Screenshot from 2023-09-16 17-18-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/557940cd-953f-452e-9c80-5506d67e6c53)
![Screenshot from 2023-09-16 17-18-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4b6235fe-dc57-4dcd-8455-7a63774c6e0c)


## 4. General timing characterization parameters
- ### Timing threshold definitions
![Screenshot from 2023-09-16 17-22-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f141ec1c-fb44-46c2-a000-0bf4b74e237d)
![Screenshot from 2023-09-16 22-42-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/18c69769-1763-4a91-8c1f-9a8f6298ad28)
![Screenshot from 2023-09-16 22-42-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/74d90f29-5fcc-4fc4-ad6e-14c689b50f77)
![Screenshot from 2023-09-16 22-42-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bac0c216-febc-48cd-9daf-491625286e98)
![Screenshot from 2023-09-16 22-43-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/121df024-7e82-4a24-94f7-5aa8a308e8c7)
![Screenshot from 2023-09-16 22-44-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6af87c0b-fe3e-4866-a6c3-b36873fa09ec)
![Screenshot from 2023-09-16 22-45-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c2ed4515-2ff3-4d91-a830-83fc297be545)
![Screenshot from 2023-09-16 22-45-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/adee4b1f-8020-4d52-ad1d-68575020082b)     
- ### Propagation delay and transition time
![Screenshot from 2023-09-16 22-52-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/47727743-2d2a-40f5-9352-1f9eb6af3653)
![Screenshot from 2023-09-16 22-52-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f968eb29-95d8-46f5-83c3-5d2b31488ff8)
![Screenshot from 2023-09-16 22-55-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/18585568-0494-4b0a-b4fd-a62e772a76b5)
![Screenshot from 2023-09-16 22-55-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/33503f6a-00f7-4b20-87b4-6fccd304179a)
![Screenshot from 2023-09-16 22-57-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8001149a-7ebb-4c0a-9366-d1ad5e1b2da5)
![Screenshot from 2023-09-16 22-58-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4ee86602-fcb0-4851-9972-adff4f38f143)
![Screenshot from 2023-09-16 22-58-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6e860fe3-36b8-4b01-be2e-fa58459ac5a8)
![Screenshot from 2023-09-16 23-00-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0a0a3ac5-08f4-4211-897b-120894dada9c)
</details>




<details>
<summary> WEEK-3 -> Day - 3 </summary>

# Design library cell using Magic Layout and ngspice characterization 

## 1. Labs for CMOS inverter ngspice simulations
       
- ###  IO placer revision 
![VirtualBox_PES_physical_design_17_09_2023_08_02_15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5320d97f-5c0f-4159-ba65-a2ffe7b96892)
![VirtualBox_PES_physical_design_17_09_2023_08_18_53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/910e6c0a-92ae-4e8b-a6ad-8114f06db3e0)
![VirtualBox_PES_physical_design_17_09_2023_08_18_24](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4bb9fd09-7e70-41da-bd7b-d01439bd5998)
![VirtualBox_PES_physical_design_17_09_2023_08_18_44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bd004446-366c-460d-8793-56ac1f4a1fbf)
![VirtualBox_PES_physical_design_17_09_2023_08_22_31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c8745a83-6a81-4435-bb78-cac12f090de7)
- ### SPICE deck creation for CMOS inverter 
![Screenshot from 2023-09-17 08-27-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/584f6131-92bd-44ca-9de4-e33ee3a47932)
![Screenshot from 2023-09-17 09-09-33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/15ddd21e-9062-4e84-9225-eb7d990a3c92)
![Screenshot from 2023-09-17 09-12-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/87640242-6b83-4b8c-b7f7-0eb4a85854d6)
![Screenshot from 2023-09-17 09-13-10](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4aabf6ca-ec5f-4d06-944c-4395ae205801)
- ### SPICE simulation lab for CMOS inverter
![Screenshot from 2023-09-17 09-25-41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3efe7dd4-46b8-41ca-b0e2-6529994dfb57)
![Screenshot from 2023-09-17 09-26-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8a1e8e33-bb01-4ce2-a136-499dc8fbcf8b)
![Screenshot from 2023-09-17 09-27-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2fb6869b-e374-4a4c-a0ca-5bb0bce89fb5)
![Screenshot from 2023-09-17 09-27-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/04a7979a-1d85-4096-83ae-de9a6934c8fb)
![Screenshot from 2023-09-17 09-28-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8063f03f-6a7c-40fc-9392-2f5a9c908048)
![Screenshot from 2023-09-17 09-29-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7ccb2542-a80f-4e18-9610-26d36517e1f6)
![Screenshot from 2023-09-17 09-30-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/30c40b50-80c8-4be0-9329-ff4417a784ca)
![Screenshot from 2023-09-17 09-31-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/af9a82ae-88b8-47cc-9870-5b1cdc1502ed)
![Screenshot from 2023-09-17 09-31-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/a7fa7857-a16e-413f-af51-81ecd1b6f125)
![Screenshot from 2023-09-17 09-31-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ab851d1d-53ad-45fe-aaeb-109488c07005)
![Screenshot from 2023-09-17 09-32-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1b4a020d-4eff-442d-9575-fc39ba92c8c2)
![Screenshot from 2023-09-17 09-32-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1d3597e7-0409-4b5c-a936-d6c89c7aea65)
![Screenshot from 2023-09-17 09-33-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b099b3ba-9124-4961-8494-b1003257e10d)
![Screenshot from 2023-09-17 09-33-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5a4c7279-0cb3-4f12-b5c1-ec846eaf339b)
![Screenshot from 2023-09-17 09-33-59](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/41f13c9a-c6ed-4c97-8b45-6edf908a5a1b)
- ### Switching Threshold Vm 
![Screenshot from 2023-09-17 09-45-44](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/94c0bd49-4cd9-4ff7-910e-ab6ca85af0bc)
![Screenshot from 2023-09-17 09-46-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/448cf589-d97f-4a5e-8fb3-b8ad71428a32)
![Screenshot from 2023-09-17 09-47-19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/eecf1403-7281-4173-b01f-9e0bc54840ec)
![Screenshot from 2023-09-17 09-47-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/07fd6867-a47c-482a-95fa-73bf9c642a7c)
![Screenshot from 2023-09-17 09-49-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/51e18153-d0ef-4388-9fe2-545b81e49411)
![Screenshot from 2023-09-17 09-50-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9451779a-c05c-4849-8f7e-6aaff4de6279)
![Screenshot from 2023-09-17 09-55-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/14574bdf-24f3-42b9-a014-7b8dd598b30f)
- ### Static and dynamic simulation of CMOS inverter 
![Screenshot from 2023-09-17 09-59-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3356dd2f-3591-4255-9170-9d06bb9a2f24)
![Screenshot from 2023-09-17 10-00-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2c5f4bbb-292e-4691-96cd-515d6a907db6)
![Screenshot from 2023-09-17 10-01-38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/93236596-b281-4544-9b18-c82f7c79c156)
![Screenshot from 2023-09-17 10-01-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ee1f3362-2f91-4aa1-9965-938c35cbbb53)
![Screenshot from 2023-09-17 10-01-53](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/652e08cb-5d08-440b-b739-396e1403082a)
![Screenshot from 2023-09-17 10-02-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f7c17070-9045-4ca7-8006-eed5773dca67)
![Screenshot from 2023-09-17 10-02-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d8017a38-56dd-4426-b326-588161e2bdf5)
![Screenshot from 2023-09-17 12-47-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/21c6665d-d089-4e50-bf18-a7af527b0a79)
![Screenshot from 2023-09-17 12-48-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b5f7b653-3771-4588-b9ae-247dd6a2dcd8)
![Screenshot from 2023-09-17 12-48-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1cfb6048-873b-4ce8-b59b-ae7f7bf09214)
![Screenshot from 2023-09-17 12-50-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4e7120b2-1a73-4163-b22e-047c47a7ef74)
![Screenshot from 2023-09-17 12-50-04](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7362037c-e188-49f8-a90d-6aa4faa5be1f)
![Screenshot from 2023-09-17 12-50-09](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5c50c24b-40e6-4555-9154-6aabcfed95a4)
![Screenshot from 2023-09-17 12-50-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6846c8d5-de66-488c-97fd-433dc5097ab6)
![Screenshot from 2023-09-17 12-50-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b511ec53-2ba4-4229-bcc8-1eeae4e5d8a2)
![Screenshot from 2023-09-17 12-51-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/eba7801e-d02a-4c88-af20-4a3d1ad3f74f)
![Screenshot from 2023-09-17 12-51-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/360bf410-e0c4-4945-bca3-f323a954df5d)
![Screenshot from 2023-09-17 12-53-00](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d36e133b-5e8f-40aa-a241-7d5ea640dea1)
![Screenshot from 2023-09-17 12-54-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5e654017-c92c-411b-8582-927bbe84e1f0)
- ### Lab steps to git clone vsdstdcelldesign
![VirtualBox_PES_physical_design_17_09_2023_13_10_41](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5c9ba5e4-f649-4f13-8264-bf0c57c5c318)
![VirtualBox_PES_physical_design_17_09_2023_13_15_06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/15c54af6-eaf7-4c6e-8518-24fce048e895)
![VirtualBox_PES_physical_design_17_09_2023_13_17_52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ec4521f6-5e1c-4a91-a1e0-3e28deaa32c7)
![VirtualBox_PES_physical_design_17_09_2023_13_17_45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/43e4c943-17a8-4533-8370-5c67f6618bfb)

## 2. Inception of Layout Â CMOS fabrication process

   
- ### Create Active regions
  
![Screenshot from 2023-09-17 14-02-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/51dc8d17-830c-4046-a3ba-ad9c33fab963)
![Screenshot from 2023-09-17 14-22-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/eac917c2-0bfb-4dc8-9bb1-26f269ee578a)
![Screenshot from 2023-09-17 14-24-48](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8b35eba8-a0a8-466c-b459-26f2c6dce6fa)
![Screenshot from 2023-09-17 14-24-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2a92feeb-5345-497a-9f6f-b060dc9d2371)
![Screenshot from 2023-09-17 14-28-51](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/31dc95b9-0864-43ff-911e-e311ebf4a7c9)
![Screenshot from 2023-09-17 14-29-02](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/db3c0927-b86c-452f-9329-6325548190e4)
![Screenshot from 2023-09-17 14-30-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f4a9c873-7953-40a8-95fc-44f262877693)
![Screenshot from 2023-09-17 14-31-16](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b8eddfa3-3fc8-47e4-9274-0e9f15bf89a3)
![Screenshot from 2023-09-17 14-31-22](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/4c2fa1a8-ae42-43c4-989f-4c1ae38c256e)
![Screenshot from 2023-09-17 14-31-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/382c50d4-d9d1-47ef-a365-075992fce5e8)
![Screenshot from 2023-09-17 14-32-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/56fd2c77-b609-4141-916e-a3fc0db05065)

- ### Formation of N-well and P-well
![Screenshot from 2023-09-17 14-55-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8c37ecc3-5600-4e25-9e46-43e91f8264d9)
![Screenshot from 2023-09-17 14-56-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/154ba139-2e9b-4833-9575-7b4859ed8722)
![Screenshot from 2023-09-17 14-57-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/34cc532b-9c4f-4dce-b04e-ba45d776aa9d)
![Screenshot from 2023-09-17 14-57-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f9e0356e-622e-468e-80af-ba3043a68477)
![Screenshot from 2023-09-17 14-58-05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cf2caaef-7ea3-492d-835e-44bf6a6e17ce)
![Screenshot from 2023-09-17 14-58-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d1875f83-9792-462d-8839-15278d65fc15)
![Screenshot from 2023-09-17 14-59-38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3130af16-fc66-4a1b-86ab-c1cfc45a11ee)
![Screenshot from 2023-09-17 15-00-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f2920eaa-d8cb-4693-b909-06b4cf698005)
![Screenshot from 2023-09-17 15-00-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b3625252-2a48-4b68-80e0-f210a60461b0)
![Screenshot from 2023-09-17 15-01-11](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/53e72c19-8526-440b-9550-39e7a3e29b1d)
![Screenshot from 2023-09-17 15-01-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6be644a4-2556-46fd-9c46-2133e99b59b4)



- ### Formation of gate terminal

![Screenshot from 2023-09-17 14-36-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8da55799-f6f8-4b3b-beb7-d1591af856a6)
![Screenshot from 2023-09-17 14-38-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c39035af-ac8d-4549-854b-df067b70cd7b)
![Screenshot from 2023-09-17 14-40-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/65998b46-a72e-48f1-b45b-8756465c82cb)
![Screenshot from 2023-09-17 14-42-35](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7041adb4-294c-4463-a73c-a5951dc14273)
![Screenshot from 2023-09-17 14-43-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7114d3a2-bb22-45f6-b981-cd2817ad9b65)
![Screenshot from 2023-09-17 14-43-29](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/56201cff-ee63-4de8-ad3a-f1106313c6b1)
![Screenshot from 2023-09-17 14-44-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2b0ed540-4e7c-4cbe-971c-9f3140ba4cbb)
![Screenshot from 2023-09-17 14-44-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1b55455c-d35a-4d75-902d-3af8bafa4ee0)
![Screenshot from 2023-09-17 14-45-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7b492042-9050-4e6a-8835-d3a746bc274b)
![Screenshot from 2023-09-17 14-45-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/d90b570c-180e-4fee-8ac9-fe420f9466fb)
![Screenshot from 2023-09-17 14-45-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/69db8c43-fb23-4cd6-a03b-e311a4157d5b)
![Screenshot from 2023-09-17 14-46-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/93d07f74-e82d-4f24-9bfa-907fabdea0fa)
![Screenshot from 2023-09-17 14-47-38](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3c73351d-6f1b-4314-82ae-2dbbceea3a1e)

- ### Lightly doped drain (LDD) formation
  
   ![Screenshot from 2023-09-17 17-43-21](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3463530e-7ac0-413a-815f-0985ebd70ce6)
![Screenshot from 2023-09-17 18-08-37](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c550200e-8144-4e1d-9f53-313d1f1b65b2)
![Screenshot from 2023-09-17 18-11-30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5a1d36b6-4a04-4406-8785-448fae4ba7b6)
![Screenshot from 2023-09-17 18-12-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/524e87a8-0294-4d80-a462-8d9b4f646434)
![Screenshot from 2023-09-17 18-12-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8924b955-bfe8-4673-9d96-07985349acd7)
![Screenshot from 2023-09-17 18-13-18](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/591d55e9-81e4-462a-8ee5-0f9d0c5f128e)
![Screenshot from 2023-09-17 18-13-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/33e33099-3422-47fb-ba40-d9488b976396)
![Screenshot from 2023-09-17 18-14-55](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6ea258e7-cf28-4e9c-a82e-e1e06496978e)
![Screenshot from 2023-09-17 18-15-15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/125579c8-af0b-4746-9749-d333138a3b53)
![Screenshot from 2023-09-17 18-15-52](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/909c0f82-b205-41a8-8cca-f065de33e44a)
![Screenshot from 2023-09-17 18-16-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7f12058d-416a-49e2-b50e-16856a5f892a)
![Screenshot from 2023-09-17 18-16-31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bcd30a3a-6d81-460f-9e4a-f7648c3079e8)
![Screenshot from 2023-09-17 18-17-08](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e1f2988e-5869-4c92-a440-b818ac69bd9b)


- ### Source Â drain formation

![Screenshot from 2023-09-17 18-20-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3356dabe-2447-4e84-aac4-00b7a7cc26cc)
![Screenshot from 2023-09-17 18-20-51](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7ab3f556-52e3-4427-bf4b-c17d96474c53)
![Screenshot from 2023-09-17 18-21-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/85efd251-613b-4c39-b05c-a714a139e05d)
![Screenshot from 2023-09-17 18-22-56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7ec5e87b-9b2b-4fc3-b971-d132e9f1818e)
![Screenshot from 2023-09-17 18-23-50](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5d35c097-9680-49f3-be61-7a38d9969582)
![Screenshot from 2023-09-17 18-24-12](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e2215ffb-7ddc-4a9d-808f-71b69feafcc9)
![Screenshot from 2023-09-17 18-24-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/11f0429f-6c04-4949-8d37-e181d43b5f4e)
![Screenshot from 2023-09-17 18-25-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ab1de2a1-7c9b-416d-8258-cddf0a34c705)
![Screenshot from 2023-09-17 18-25-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b4ab0756-cbe7-4284-9165-26bf42a3f1ac)


- ### Local interconnect formation 
![Screenshot from 2023-09-17 18-25-25](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6149704a-4571-4493-a124-64473b0d3cbf)
![Screenshot from 2023-09-17 18-29-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2db47b99-f37c-4db6-9e4e-48b1383f07ef)
![Screenshot from 2023-09-17 18-30-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7da1638c-48fe-47ea-a950-143a08a62b4a)
![Screenshot from 2023-09-17 18-31-01](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/2a11d103-e5ce-4b8f-afdb-8e0b0d926749)
![Screenshot from 2023-09-17 18-31-42](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ce93ff75-6ee0-4da7-9b18-7d2992b66f78)
![Screenshot from 2023-09-17 18-31-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0702c4bc-b929-422a-9080-12d91407a944)
![Screenshot from 2023-09-17 18-32-43](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f62e40d1-313c-4dc6-b5e5-79591366bd2d)
![Screenshot from 2023-09-17 18-32-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0774864b-c999-4d24-9c79-f488e8d0d31b)
![Screenshot from 2023-09-17 18-34-26](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/51419184-3bbf-41e0-971b-15649a63e02b)
![Screenshot from 2023-09-17 18-35-14](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/7c757ff9-26dc-4f66-86de-0662048ae27a)
![Screenshot from 2023-09-17 18-35-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/84251179-56e0-4a30-ad2c-a27075fb53fa)
![Screenshot from 2023-09-17 18-35-33](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c78d915a-8618-4864-887e-46fbbee47a77)
![Screenshot from 2023-09-17 18-36-23](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b532f61b-6cef-4355-bbd9-a5a24f1d9c63)
![Screenshot from 2023-09-17 18-36-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/87dd81bd-a13e-4a64-8479-6c0b7a7bb079)


- ### Higher level metal formation
  
![Screenshot from 2023-09-17 18-36-46](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/eee39e58-d1a1-4181-b4eb-f61304f98c29)
![Screenshot from 2023-09-17 19-04-47](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6647890b-b98a-4e70-89db-5b6833d2eb2d)
![Screenshot from 2023-09-17 19-05-58](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1ce3a6e7-8b2b-4763-bc7b-e52b3c3cab6a)
![Screenshot from 2023-09-17 19-12-57](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e759f551-5f89-437d-b4e7-6022b0699013)
![Screenshot from 2023-09-17 19-14-13](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5dfa4e37-74dd-4093-85d3-7fc3f9955292)
![Screenshot from 2023-09-17 19-14-34](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/5db1f4f5-862c-4028-80d9-ba359e16ca8d)
![Screenshot from 2023-09-17 19-14-39](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cf07dfe2-7958-44e5-b1d5-1d32139344e0)
![Screenshot from 2023-09-17 19-15-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/b6e57dbd-7c28-448a-a1f5-7242ea66a908)
![Screenshot from 2023-09-17 19-15-27](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/cb32b608-0370-47ef-beed-e45ee2ecbb2f)
![Screenshot from 2023-09-17 19-15-36](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/1c16d4b9-874b-4a68-bedc-cbbbeae2a1a5)
![Screenshot from 2023-09-17 19-16-54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e7ef238b-4fe5-45ad-bfad-a6954890086a)
![Screenshot from 2023-09-17 19-17-05](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/9bf3bd36-cda9-43cd-8683-86f7c6b2272d)
![Screenshot from 2023-09-17 19-17-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/64de6b1d-18b5-4dff-8797-d590218d90b2)
![Screenshot from 2023-09-17 19-17-20](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/f739aaad-25c1-4856-a893-6c5588c21425)
![Screenshot from 2023-09-17 19-17-28](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8988db4f-6ecd-417d-ba71-135dc4a88813)
![Screenshot from 2023-09-17 19-17-45](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/0c396d72-cbf8-44f7-84c6-e573e4921509)
![Screenshot from 2023-09-17 19-18-06](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/fadfcb56-5caa-4775-8ba3-8de8c05cdb76)
![Screenshot from 2023-09-17 19-21-07](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/c067b55f-e25e-4ebb-8e47-4be3b62e2a50)
![Screenshot from 2023-09-17 19-21-49](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/50503440-9bc8-4726-b41a-ed828d0df5a0)
![Screenshot from 2023-09-17 19-22-32](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e707e809-6e1f-4371-a6a7-fec3f5244065)
![Screenshot from 2023-09-17 19-23-17](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/3fadd29b-d8e2-48ed-8a11-a7d782a91109)
![Screenshot from 2023-09-17 19-23-40](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/e42bb111-da32-47a5-bdcd-38a848530368)
![Screenshot from 2023-09-17 19-24-09](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/ede4f858-86f2-47be-aab3-9ebfcf6c3a5c)

- ### Lab introduction to Sky130 basic layers layout and LEF using inverter 


 ![VirtualBox_PES_physical_design_17_09_2023_19_55_15](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8f7a53a1-4984-4e9c-874e-68763239881a)
![VirtualBox_PES_physical_design_17_09_2023_19_56_19](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/6b6dbbbc-5835-4042-be4c-61624a81ceec)
![VirtualBox_PES_physical_design_17_09_2023_19_57_31](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/bc10c9e5-7c17-47dc-8765-4d4871020caf)
![VirtualBox_PES_physical_design_17_09_2023_19_59_56](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/76c853ad-0e02-4b9b-a712-b1a95592f8a6)
![VirtualBox_PES_physical_design_17_09_2023_20_01_30](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/8ad814f6-326e-45fb-8102-784a5792ff54)
![VirtualBox_PES_physical_design_17_09_2023_20_01_54](https://github.com/Abhi9108865162/pes_asic_class/assets/141741065/46236685-75dd-4a76-87ba-030d2c239332)




- ### Lab steps to create std cell layout and extract spice netlist 
   



    
   
  

## 3. Sky130 Tech File Labs
- ### Lab steps to create final SPICE deck using Sky130 tech
   
- ### Lab steps to characterize inverter using sky130 model files

- ### Lab introduction to Magic tool options and DRC rules
     
- ### Lab introduction to Sky130 pdk's and steps to download labs 
   
- ### Lab introduction to Magic and steps to load Sky130 tech-rules
   
- ### Lab exercise to fix poly.9 error in Sky130 tech-file 

- ### Lab exercise to implement poly resistor spacing to diff and tap 
   
- ### Lab challenge exercise to describe DRC error as geometrical construct
   
- ### Lab challenge to find missing or incorrect rules and fix them

</details>

<details>
<summary> WEEK-3 -> Day - 4 </summary>

# Pre-layout timing analysis and importance of good clock tree 


## 1. Timing modelling using delay tables
    -

## 2. Timing analysis with ideal clocks using openSTA
    -

## 3. Clock tree synthesis TritonCTS and signal integrity
- ### Clock tree routing and buffering using H-Tree algorithm

- ### Crosstalk and clock net shielding

- ### Lab steps to run CTS using TritonCTS

- ### Lab steps to verify CTS runs 

## 4. Timing analysis with real clocks using openSTA 
- ### Setup timing analysis using real clocks

- ### Hold timing analysis using real clocks 

- ### Lab steps to analyze timing with real clocks using OpenSTA

- ### Lab steps to execute OpenSTA with right timing libraries and CTS assignment 

- ### Lab steps to observe impact of bigger CTS buffers on setup and hold timing



</details>






<details>
<summary> WEEK-3 -> Day - 5 </summary>

# Final steps for RTL2GDS using tritonRoute and openSTA 


## 1. Routing and design rule check (DRC)
- ### Introduction to Maze Routing Â LeeÂs algorithm
  
- ### LeeÂs Algorithm conclusion

- ### Design Rule Check
  
## 2. Power Distribution Network and routing
- ### Lab steps to build power distribution network

- ### Lab steps from power straps to std cell power 

- ### Basics of global and detail routing and configure TritonRoute 
## 3. TritonRoute Features
- ### TritonRoute feature 1 - Honors pre-processed route guides
   
- ### TritonRoute Feature2 & 3 - Inter-guide connectivity and intra- & inter-layer routing
   
- ### TritonRoute method to handle connectivity 
   
- ### Routing topology algorithm and final files list post-route
    
   



</details>





