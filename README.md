[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/IAASVEAZ)

# CSIT5970 Assignment-1: EC2 Measurement (2 questions, 4 marks)

### Deadline: 11:59PM, Feb, 28, Friday

---

### Name: LIU Runrong
### Student Id: 21111369
### Email: rliubk@connect.ust.hk

---

## Question 1: Measure the EC2 CPU and Memory performance

1. (1 mark) Report the name of measurement tool used in your measurements (you are free to choose *any* open source measurement software as long as it can measure CPU and memory performance). Please describe your configuration of the measurement tool, and explain why you set such a value for each parameter. Explain what the values obtained from measurement results represent (e.g., the value of your measurement result can be the execution time for a scientific computing task, a score given by the measurement tools or something else).

    Ans:

    > php-zip
    >
    > 
    >
    > ### Measurement Tool:
    >
    > I used the **Phoronix Test Suite**, an open-source benchmarking tool for CPU and memory performance.
    >
    > ### Configuration:
    >
    > - **Test Selected**: `compress-7zip` to measure CPU and memory performance during compression and decompression tasks.
    > - **Iterations**: 3 iterations to ensure consistent results.
    > - **Timeout**: No specific timeout set; the benchmark handles timeouts internally.
    >
    > ### Explanation of Results:
    >
    > - **Compression Rating (MIPS)**: Average of 4238 MIPS, indicating CPU efficiency in compression tasks.
    > - **Decompression Rating (MIPS)**: Average of 3176 MIPS, reflecting the system's decompression performance.

    

    console output:

    > ubuntu@ip-172-31-95-241:~$ phoronix-test-suite run pts/compress-7zip
    >
    > 
    >
    > 
    >
    >   [PROBLEM] pts/compress-7zip-1.11.0 is not installed. 
    >
    >   Would you like to stop and install these tests now (Y/n): Y
    >
    >   Evaluating External Test Dependencies ..............................................................................
    >
    > 
    >
    > Phoronix Test Suite v10.8.4
    >
    > 
    >
    >   To Install:  pts/compress-7zip-1.11.0
    >
    > 
    >
    >   Determining File Requirements ......................................................................................
    >
    >   Searching Download Caches ..........................................................................................
    >
    > 
    >
    >   1 Test To Install
    >
    > ​    1 File To Download [1.42MB]
    >
    > ​    16MB Of Disk Space Is Needed
    >
    > ​    33 Seconds Estimated Install Time
    >
    > 
    >
    >   pts/compress-7zip-1.11.0:
    >
    > ​    Test Installation 1 of 1
    >
    > ​    1 File Needed [1.42 MB]
    >
    > ​    Downloading: 7z2405-src.tar.xz                                     [1.42MB]
    >
    > ​    Downloading ....................................................................................................
    >
    > ​    Approximate Install Size: 16 MB
    >
    > ​    Estimated Install Time: 33 Seconds
    >
    > ​    Installing Test @ 09:39:21
    >
    > 
    >
    > 
    >
    > System Information
    >
    > 
    >
    > 
    >
    >  PROCESSOR:       Intel Xeon E5-2686 v4
    >
    >   Core Count:      1                     
    >
    >   Extensions:      SSE 4.2 + AVX2 + AVX + RDRAND + FSGSBASE 
    >
    >   Cache Size:      45 MB                   
    >
    >   Microcode:      0xd0003f6                 
    >
    >   Core Family:     Broadwell                 
    >
    > 
    >
    >  GRAPHICS:        Cirrus Logic GD 5446
    >
    >   Vulkan:        1.3.255      
    >
    > 
    >
    >  MOTHERBOARD:      Xen HVM domU
    >
    >   BIOS Version:     4.11.amazon       
    >
    >   Chipset:       Intel 440FX 82441FX PMC 
    >
    > 
    >
    >  MEMORY:         1024MB
    >
    > 
    >
    >  DISK:          31GB
    >
    >   File-System:     ext4                  
    >
    >   Mount Options:    discard errors=remount-ro relatime rw 
    >
    >   Disk Details:     Block Size: 4096            
    >
    > 
    >
    >  OPERATING SYSTEM:    Ubuntu 22.04
    >
    >   Kernel:        6.8.0-1021-aws (x86_64)                                             
    >
    >   Compiler:       GCC 11.4.0                                                    
    >
    >   System Layer:     Xen HVM domU 4.11.amazon                                             
    >
    >   Security:       gather_data_sampling: Not affected                                        
    >
    > ​             \+ itlb_multihit: KVM: Mitigation of VMX unsupported                               
    >
    > ​             \+ l1tf: Mitigation of PTE Inversion                                       
    >
    > ​             \+ mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                 
    >
    > ​             \+ meltdown: Mitigation of PTI                                          
    >
    > ​             \+ mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown           
    >
    > ​             \+ reg_file_data_sampling: Not affected                                      
    >
    > ​             \+ retbleed: Not affected                                             
    >
    > ​             \+ spec_rstack_overflow: Not affected                                       
    >
    > ​             \+ spec_store_bypass: Vulnerable                                         
    >
    > ​             \+ spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization               
    >
    > ​             \+ spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
    >
    > ​             \+ srbds: Not affected                                              
    >
    > ​             \+ tsx_async_abort: Not affected                                         
    >
    > 
    >
    >   Would you like to save these test results (Y/n): Y
    >
    >   Enter a name for the result file: 1
    >
    >   Enter a unique name to describe this test run / configuration: 1
    >
    > 
    >
    > If desired, enter a new description below to better describe this result set / system configuration under test.
    >
    > Press ENTER to proceed without changes.
    >
    > 
    >
    > Current Description: Xen HVM domU 4.11.amazon testing on Ubuntu 22.04 via the Phoronix Test Suite.
    >
    > 
    >
    > New Description: 1
    >
    > 
    >
    > 7-Zip Compression 24.05:
    >
    >   pts/compress-7zip-1.11.0
    >
    >   Test 1 of 1
    >
    >   Estimated Trial Run Count:  3            
    >
    >   Estimated Time To Completion: 17 Minutes [09:57 UTC] 
    >
    > ​    Started Run 1 @ 09:41:10
    >
    > ​    Started Run 2 @ 09:41:55
    >
    > ​    Started Run 3 @ 09:42:40
    >
    > 
    >
    >   Test: Compression Rating:
    >
    > ​    4283
    >
    > ​    4255
    >
    > ​    4175
    >
    > 
    >
    >   Average: 4238 MIPS
    >
    >   Deviation: 1.32%
    >
    > 
    >
    >   Comparison of 2,165 OpenBenchmarking.org samples since 10 May 2024; median result: 94132 MIPS. Box plot of samples:
    >
    >   [--######!#########----------------------------*--------------------------*--*-*---*--------------------|    *   ]
    >
    > ​            2 x AMD EPYC 9275F: 507917 ^    2 x AMD EPYC 9475F: 899868 ^ 2 x AMD EPYC 9655: 1219921 ^
    >
    > ​                               AMD EPYC 9845: 857791 ^
    >
    > ​                          2 x Intel Xeon 6980P: 833643 ^
    >
    > ​                          2 x AMD EPYC 9754: 799824 ^
    >
    > 
    >
    > 
    >
    >   Test: Decompression Rating:
    >
    > ​    3178
    >
    > ​    3176
    >
    > ​    3174
    >
    > 
    >
    >   Average: 3176 MIPS
    >
    >   Deviation: 0.06%
    >
    > 
    >
    >   Comparison of 2,128 OpenBenchmarking.org samples since 10 May 2024; median result: 76860 MIPS. Box plot of samples:
    >
    >   [-####!#######---------------------------------------------*------------*--*-*-----------*-------------|       *]
    >
    > ​                 2 x Intel Xeon 6766E: 776612 ^ 2 x AMD EPYC 9654: 1178644 ^ 2 x AMD EPYC 9825: 1557636 ^
    >
    > ​                           2 x AMD EPYC 9565: 1021036 ^
    >
    > ​                             AMD EPYC 9965: 998566 ^
    >
    > ​                         2 x AMD EPYC 9534: 949019 ^
    >
    > 
    >
    >   Do you want to view the text results of the testing (Y/n): Y
    >
    > 1
    >
    > 1
    >
    > 
    >
    > 
    >
    > 1: 
    >
    > 
    >
    > ​	Processor: Intel Xeon E5-2686 v4 (1 Core), Motherboard: Xen HVM domU (4.11.amazon BIOS), Chipset: Intel 440FX 82441FX PMC, Memory: 1024MB, Disk: 31GB, Graphics: Cirrus Logic GD 5446
    >
    > 
    >
    > ​	OS: Ubuntu 22.04, Kernel: 6.8.0-1021-aws (x86_64), Vulkan: 1.3.255, Compiler: GCC 11.4.0, File-System: ext4, System Layer: Xen HVM domU 4.11.amazon
    >
    > 
    >
    > 
    >
    >   7-Zip Compression 24.05
    >
    >   Test: Compression Rating
    >
    >   MIPS > Higher Is Better
    >
    >   1 . 4238 |==============================================================================================================
    >
    > 
    >
    > 
    >
    >   7-Zip Compression 24.05
    >
    >   Test: Decompression Rating
    >
    >   MIPS > Higher Is Better
    >
    >   1 . 3176 |==============================================================================================================

    

    

    > ubuntu@ip-172-31-95-241:~$ phoronix-test-suite run pts/ramspeed
    >
    > 
    >
    > 
    >
    > 
    >
    > RAMspeed SMP 3.5.0:
    >
    >   pts/ramspeed-1.4.3
    >
    >   Memory Test Configuration
    >
    > ​    1: Copy
    >
    > ​    2: Scale
    >
    > ​    3: Add
    >
    > ​    4: Triad
    >
    > ​    5: Average
    >
    > ​    6: Test All Options
    >
    > ​    ** Multiple items can be selected, delimit by a comma. **
    >
    > ​    Type: 1
    >
    > 
    >
    > 
    >
    > ​    1: Integer
    >
    > ​    2: Floating Point
    >
    > ​    3: Test All Options
    >
    > ​    ** Multiple items can be selected, delimit by a comma. **
    >
    > ​    Benchmark: 1
    >
    > 
    >
    > 
    >
    > Phoronix Test Suite v10.8.4
    >
    > System Information
    >
    > 
    >
    > 
    >
    >  PROCESSOR:       Intel Xeon E5-2686 v4
    >
    >   Core Count:      1                     
    >
    >   Extensions:      SSE 4.2 + AVX2 + AVX + RDRAND + FSGSBASE 
    >
    >   Cache Size:      45 MB                   
    >
    >   Microcode:      0xd0003f6                 
    >
    >   Core Family:     Broadwell                 
    >
    > 
    >
    >  GRAPHICS:        Cirrus Logic GD 5446
    >
    >   Vulkan:        1.3.255      
    >
    > 
    >
    >  MOTHERBOARD:      Xen HVM domU
    >
    >   BIOS Version:     4.11.amazon       
    >
    >   Chipset:       Intel 440FX 82441FX PMC 
    >
    > 
    >
    >  MEMORY:         1024MB
    >
    > 
    >
    >  DISK:          31GB
    >
    >   File-System:     ext4                  
    >
    >   Mount Options:    discard errors=remount-ro relatime rw 
    >
    >   Disk Details:     Block Size: 4096            
    >
    > 
    >
    >  OPERATING SYSTEM:    Ubuntu 22.04
    >
    >   Kernel:        6.8.0-1021-aws (x86_64)                                             
    >
    >   Compiler:       GCC 11.4.0                                                    
    >
    >   System Layer:     Xen HVM domU 4.11.amazon                                             
    >
    >   Security:       gather_data_sampling: Not affected                                        
    >
    > ​             \+ itlb_multihit: KVM: Mitigation of VMX unsupported                               
    >
    > ​             \+ l1tf: Mitigation of PTE Inversion                                       
    >
    > ​             \+ mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                 
    >
    > ​             \+ meltdown: Mitigation of PTI                                          
    >
    > ​             \+ mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown           
    >
    > ​             \+ reg_file_data_sampling: Not affected                                      
    >
    > ​             \+ retbleed: Not affected                                             
    >
    > ​             \+ spec_rstack_overflow: Not affected                                       
    >
    > ​             \+ spec_store_bypass: Vulnerable                                         
    >
    > ​             \+ spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization               
    >
    > ​             \+ spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
    >
    > ​             \+ srbds: Not affected                                              
    >
    > ​             \+ tsx_async_abort: Not affected                                         
    >
    > 
    >
    >   Would you like to save these test results (Y/n): Y
    >
    > 
    >
    >   Recently Saved Test Results:
    >
    > ​    memtest  [Today]
    >
    > ​    1     [Today]
    >
    > 
    >
    >   Enter a name for the result file: 1
    >
    > 
    >
    > Current Test Identifiers:
    >
    > \- 1
    >
    > 
    >
    >   Enter a unique name to describe this test run / configuration: 1
    >
    > 
    >
    > If desired, enter a new description below to better describe this result set / system configuration under test.
    >
    > Press ENTER to proceed without changes.
    >
    > 
    >
    > Current Description: Xen HVM domU 4.11.amazon testing on Ubuntu 22.04 via the Phoronix Test Suite.
    >
    > 
    >
    > New Description: 1
    >
    > 
    >
    > RAMspeed SMP 3.5.0:
    >
    >   pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Integer]
    >
    >   Test 1 of 1
    >
    >   Estimated Trial Run Count:  3           
    >
    >   Estimated Time To Completion: 7 Minutes [10:08 UTC] 
    >
    > ​    Started Run 1 @ 10:01:56
    >
    > ​    Started Run 2 @ 10:04:39
    >
    > ​    Started Run 3 @ 10:07:21
    >
    > 
    >
    >   Type: Copy - Benchmark: Integer:
    >
    > ​    11370.96
    >
    > ​    11369.33
    >
    > ​    11359.89
    >
    > 
    >
    >   Average: 11366.73 MB/s
    >
    >   Deviation: 0.05%
    >
    > 
    >
    >   Comparison of 6,168 OpenBenchmarking.org samples since 26 February 2011; median result: 19022 MB/s. Box plot of samples:
    >
    >   [  |------------*###########!##########-*-*-*-----*--------------------------------*----*|  *    *      * ]
    >
    > ​           ^ This Result (20th Percentile): 11367
    >
    > ​             8 x 16 GB DDR4-2667MT: 33438 ^  2 x 16 GB DDR5-7200MT: 54685 ^ 1 x 480GB DRAM-6400MT: 75690 ^
    >
    > ​          12 x 32 GB DDR4-3200MT: 29730 ^               2 x 32GB DDR5-5600MT: 68005 ^
    >
    > ​           8 x GB DDR4-3200MT: 28432 ^            2 x 16GB DDR5-8000MT: 61883 ^
    >
    > ​       6 x 4096 MB DDR4-2666MT: 26784 ^         2 x 16 GB DDR4-3733MT: 58210 ^
    >
    > 
    >
    >   Do you want to view the text results of the testing (Y/n): Y
    >
    > 1
    >
    > 1
    >
    > 
    >
    > 
    >
    > 1: 
    >
    > 
    >
    > ​	Processor: Intel Xeon E5-2686 v4 (1 Core), Motherboard: Xen HVM domU (4.11.amazon BIOS), Chipset: Intel 440FX 82441FX PMC, Memory: 1024MB, Disk: 31GB, Graphics: Cirrus Logic GD 5446
    >
    > 
    >
    > ​	OS: Ubuntu 22.04, Kernel: 6.8.0-1021-aws (x86_64), Vulkan: 1.3.255, Compiler: GCC 11.4.0, File-System: ext4, System Layer: Xen HVM domU 4.11.amazon
    >
    > 
    >
    > 
    >
    >   7-Zip Compression 24.05
    >
    >   Test: Compression Rating
    >
    >   MIPS > Higher Is Better
    >
    >   1 . 4238 |==============================================================================================================
    >
    > 
    >
    > 
    >
    >   7-Zip Compression 24.05
    >
    >   Test: Decompression Rating
    >
    >   MIPS > Higher Is Better
    >
    >   1 . 3176 |==============================================================================================================
    >
    > 
    >
    > 
    >
    >   RAMspeed SMP 3.5.0
    >
    >   Type: Copy - Benchmark: Integer
    >
    >   MB/s > Higher Is Better
    >
    >   1 . 11366.73 |==========================================================================================================
    >
    > 
    >
    > 

    

2. (1 mark) Run your measurement tool on general purpose `t2.micro`, `t2.medium`, and `c5d.large` Linux instances, respectively, and find the performance differences among these instances. Launch all the instances in the **US East (N. Virginia)** region. Does the performance of EC2 instances increase commensurate with the increase of the number of vCPUs and memory resource?

    In order to answer this question, you need to complete the following table by filling out blanks with the measurement results corresponding to each instance type.

    | Size        | CPU performance | Memory performance |
    | ----------- | --------------- | ------------------ |
    | `t2.micro` | 3176 MIPS | 11366.73 MB/s |
    | `t2.medium`  | 10255 MIPS | 19804.60 MB/s |
    | `c5d.large` | 5331 MIPS | 14821.56 MB/s |

    > Region: US East (N. Virginia). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI.

## Question 2: Measure the EC2 Network performance

1. (1 mark) The metrics of network performance include **TCP bandwidth** and **round-trip time (RTT)**. Within the same region, what network performance is experienced between instances of the same type and different types? In order to answer this question, you need to complete the following table.

    | Type                      | TCP b/w (Mbps) | RTT (ms) |
    | ------------------------- | -------------- | -------- |
    | `t3.medium` - `t3.medium` | 3780           | 0.249    |
    | `m5.large` - `m5.large`   | 2750           | 0.649    |
    | `c5n.large` - `c5n.large` | 4940           | 0.224    |
    | `t3.medium` - `c5n.large` | 2230           | 0.749    |
    | `m5.large` - `c5n.large`  | 4940           | 0.138    |
    | `m5.large` - `t3.medium`  | 2420           | 0.678    |

    > Region: US East (N. Virginia). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI. Note: Use private IP address when using iPerf within the same region. You'll need iPerf for measuring TCP bandwidth and Ping for measuring Round-Trip time.

2. (1 mark) What about the network performance for instances deployed in different regions? In order to answer this question, you need to complete the following table.

    | Connection                | TCP b/w (Mbps) | RTT (ms) |
    | ------------------------- | -------------- | -------- |
    | N. Virginia - Oregon      | 32.7           | 62.4     |
    | N. Virginia - N. Virginia | 2600           | 0.556    |
    | Oregon - Oregon           | 4740           | 0.191    |

    > Region: US East (N. Virginia), US West (Oregon). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI. All instances are `c5.large`. Note: Use public IP address when using iPerf within the same region.
