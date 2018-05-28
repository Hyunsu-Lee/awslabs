# awslabs
<table style="width:100%">
  <tr>
    <th width="100%" colspan="6"><h2>XUP AWS F1 Labs</h2></th>
  </tr>
  <tr>
    <td width="15%" align="center"><b>Introduction</b></td>
    <td width="15%" align="center"><a href="Connecting_to_AWS_lab.md">1. Connecting to your F1 instance</a></td> 
    <td width="15%" align="center"><a href="Makefile_Flow_lab.md">2. Makefile Flow Lab</a></td>
    <td width="15%" align="center"><a href="GUI_Flow_lab.md">3. GUI Flow Lab</a></td>
    <td width="15%" align="center"><a href="Optimization_lab.md">4. Optimization Lab</a><td>
    <td width="15%" align="center"><a href="rtl_kernel_wizard_lab.md">5. RTL-Kernel Wizard Lab</a><td>
  </tr>
</table>

---------------------------------------
### Introduction

Welcome to the AWS F1 Xilinx Developer Labs. During this session you will gain hands-on experience with AWS F1 and learn how to develop accelerated applications using the AWS F1 OpenCL flow and the Xilinx SDAccel development environment.

#### Overview of the AWS F1 platform and SDAccel flow

The architecture of the AWS F1 platform and the SDAccel development flow are pictured below:

![](./images/introduction/f1_platform.png)

1. Amazon EC2 F1 is a compute instance combining x86 CPUs with Xilinx FPGAs. The FPGAs are programmed with custom hardware accelerators which can accelerate complex workloads up to 30x when compared with servers that use CPUs alone. 
2. An F1 application consists of an x86 executable for the host application and an FPGA binary (also referred to as Amazon FPGA Image or AFI) for the custom hardware accelerators. Communication between the host application and the accelerators are automatically managed by the OpenCL runtime.
3. SDAccel is the development environment used to create F1 applications. It comes with a fully fledged IDE, x86 and FPGA compilers, profiling and debugging tools.
4. The host application is written in C or C++ and uses the OpenCL API to interact with the accelerated functions. The accelerated functions (also referred to as kernels) can be written in C, C++, OpenCL or even RTL.


#### Overview of the Xilinx Developer Lab modules

This developer lab is divided in 4 modules. It is recommended to complete each module before proceeding to the next.

1. **Connecting to your F1 instance** \
You will start a pre-configured EC2 F1 instance and connect to it using a remote desktop client. Once connected, you will download the lab files and confirm you can execute a simple application on F1.
1. **Experiencing F1 acceleration** \
AWS F1 instances are ideal to accelerate complex workloads. In this module you will experience the potential of F1 by using FFmpeg to run both a software implementation and an F1-optimized implementation of an H.265/HEVC encoder. 
1. **Developing and optimizing F1 applications with SDAccel** \
You will use the SDAccel development environment to create, profile and optimize an F1 accelerator. The lab focuses on the Inverse Discrete Cosine Transform (IDCT), a compute intensive function used at the heart of all video codecs.
1. **Wrap-up and next steps** \
You will to close your RDP session, stop your F1 instance and explore next steps to continue your F1 experience after the Xilinx Developer Lab.

Since building FPGA binaries is not instantaneous, all the modules of this Developer Lab will use precompiled FPGA binaries.

---------------------------------------

<p align="center"><b>
Start the first lab: <a href="Connecting_to_AWS_lab.md">1. Connecting to your F1 instance</a>
</b></p>

