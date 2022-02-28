# Full adder
 Full adder in Intel Quartus Prime Lite 21.1 and Questa Starter Ed.

## Settings

1. Project name: `adder01`
2. EDA: Intel Quartus Prime Lite 21.1
3. Simulation: Questa Starter Edition (Siemens)
4. License: Free license for Questa Starter Edition in file `C:\intelFPGA_lite\21.1\licenses\questa-starter\LR-072239_License.dat`
5. FPGA: DE-1 SoC Cyclone V
6. OS: Windows 10 Enterprise

## Setup

Updates to the procedure in the following two videos on YouTube for the [settings](#settings) above:  
1. [Creating a schematic diagram in Quartus Prime Lite Edition](https://www.youtube.com/watch?v=qn6ggwxpDjQ)  
2. [Creating a waveform simulation in Quartus Prime Lite Edition](https://www.youtube.com/watch?v=e_ksjHd6sY0&t=146s)  

### Admin rights

Note that you will need to have admin right for some of these operations. On my work computer, I use **Make Me Admin** and I have been added to the corresponding network user group by IT.

### Steps

1. Install Intel Quertus Prime Lite 21.1 from [download page](https://www.intel.com/content/www/us/en/software-kit/684216/intel-quartus-prime-lite-edition-design-software-version-21-1-for-windows.html?). I used the "Multiple Download" option. This is a consolidated install with the addon packages in a `components` directory. These are device support and simulation tools.  
2. Sign up for an Intel account at [My Intel](https://www.intel.com/content/www/us/en/programmable/my-intel/mal-home.html).
3. Generating the free Questa Starter Edition license:
   1. Go to the [Intel self-serve licensing center](https://licensing.intel.com/psg/s/). Click on **Sign up for Evaluation or Free Licenses**.
   2. I selected **Fixed** license for **1 seat** and registered a computer by its **NIC** (Network Interface Card) address.
   3. To obtain the NIC, open a Command Prompt window, type the command `ipconfig /all`, hit Enter, and read the code on the **Physical Address** line.
   4. Enter the NIC _without the dashes_.
   5. Download the license file that is generated. I put it in the Quartus installation directory tree as shown in the [Settings](#settings).
4. Open Quartus Prime and find **Tools-->License Setup**.
5. At the top, select the license file. Although it is supposed to supersede the **LM_LICENSE_FILE** environment variable, it doesn't.
6. Search for "environment variables" to open the **System Properties** panel. Click on **Environment Variables...**. Under _user_ variables, add a new variable **LM_LICENSE_FILE** with value the full path of the license file. Restart Quartus and check that it was added to the read-only field under the license file field.
7. Click on "New Project Wizard".
8. The first video above can now be followed for this part, except:
   1. Under **Family, Device & Board Settings** select the **Board** tab and then the **DE1-SoC Board**, unclicking **Create top-level design file.**.
   2. Under **EDA Tool Settings**, for **Simulation** select **QuestaSim**.
10. Follow the generation and compilation of the schematic from the first video.
11. Follow the waveform generation from the second video. 
12. Running the simulation:
    1. If you get an error about a missing command option, in the **Simulation Waveform Editor** click on **Restore Defaults**.
    2. If you get an error about 
