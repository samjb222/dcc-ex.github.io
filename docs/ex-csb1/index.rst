:orphan:

.. include:: /include/include.rst
.. include:: /include/include-l1.rst
.. include:: /include/include-ex-cs.rst
  
|EX-CS-LOGO| |donate-button|

.. index:: EXCSB1, EX-CSB1

******************
EX-CSB1 Express
******************

|conductor| |tinkerer| |engineer| |support-button|

.. sidebar::

  .. contents:: On this page
    :depth: 1
    :local:

Designed by the |DCC-EX| development team, the EX-CSB1 replaces up to 3 different stacked boards to provide a complete, expandible DCC and DC command station with dual 5A track outputs, integrated in programming track capability, and built-in fast WiFi for throttle control connections.

.. figure:: /_static/images/ex-csb1/csb1_render_drop_shadow.png
   :alt: DCC-EX EX-CSB1 Express
   :scale: 40%

What is the EX-CSB1 Express?
=============================

EX-CSB1 Express Overview

The EX-CSB1 Express is the first fully integrated DCC Command Station with DC PWM capabilities, developed by the DCC-EX Team. This versatile board can function as a complete command station with USB or WiFi connectivity or serve as a stand-alone booster, making it an ideal addition to any layout, including those using non-DCC-EX systems.

Key Features:

All-in-One Command Station/Booster: Compatible with DCC and capable of PWM DC output.
Built-in Fast WiFi: Supports up to 10 simultaneous throttle connections, expandable with JMRI.
Advanced Hardware: Utilizes an ESP32 microcontroller with dual DCC or PWM DC 5A outputs, including variable current limit control.
Expandable Outputs: Can accept an EX-MotorShield8874 for two additional DCC/DC PWM/PROG outputs, providing power to four total districts.
Protection & Safety: Programmable over-current protection, auto-reverser capability, and RailSync DCC input for automatic booster mode engagement.
Versatile Power Supply: Operates with a single 12V to 25V power supply for the entire system.
USB-C Interface: For easy software updates, connection to EXWebThrottle or JMRI, and logging/debugging.
Accessory Support: Qwiic/STEMMA QT 3v3 compatible I2C connector for accessories like displays and lighting.
OLED Display: Bundled graphical display for status and diagnostics, with support for additional displays.

Benefits:

Ready to Use: Pre-assembled, with no need for additional assembly or configuration.
Enhanced Performance: More memory than an Arduino Mega for complex EXRAIL automation/animation scripts.
Efficient Power Usage: Less voltage drop, ensuring more power reaches the track.
Flexible Output Management: Dynamically assign outputs to different modes (DC/DCC/Prog), with NMRA current limits.
The EX-CSB1's robust, single-PCB design includes integrated MOSFET motor drivers from Texas Instruments, providing up to 5A peak power per track output. This allows for simultaneous operation of multiple locomotives with reduced power consumption and heat generation compared to traditional systems.

With its dual role as a command station or booster, the EX-CSB1 can be strategically placed around a layout, seamlessly switching to booster mode upon detecting a RailSync input signal. This feature is particularly useful for modular layouts, ensuring smooth operation across different sections.

The system includes comprehensive protection features such as reverse polarity protection, hardware and software overcurrent protection, overvoltage protection, and thermal protection. It also provides clear status indications via LEDs for microcontroller power, track input supply, and WiFi connection status.

The EX-CSB1's built-in EXRAIL Automation and Animation capabilities enable advanced control of layout operations, including automated train routing, crossing control, signal management, and more.


Why did we make it?
====================

After seeing the success of our original EX-CommandStation software, which allowed modellers to build their own setups, we realized there was a need for something even simpler. The DCC-EX team wanted to create a solution that would appeal to a wider range of modellers, especially those who might not feel as confident with electronics or those who just prefer to spend their time enjoying their layouts instead of tinkering with tech.

We wanted to keep the sense of accomplishment that comes with a DIY project but make it much easier, smaller, and more "plug-and-play." After all, most of us would rather focus on running our trains than on troubleshooting wiring or connections. Whether you consider yourself a Conductor, Tinkerer, or Engineer, you might appreciate an all-in-one solution that saves time, space, and reduces complexity. That’s why we asked ourselves, "What features would the ideal command station have?" And that’s how the EX-CSB1 Express was born.


How can I get one?
==================

Units may be purchased from the following sources:

* In Australia, New Zealand and South East Asia from `Millennium Engineering Pty Ltd <https://www.milleng.com.au>`_
* In Europe from `Semify's Web Store <https://www.semify-eda.com/ex-motorshield8874/>`_ (based in Austria)
* In the US from the `DCC-EX Store <https://store.dcc-ex.com/>`_ or...
* from `Smart Hobby, LLC <https://www.smarthobbyllc.com/>`_. You can also find Smart Hobby on Facebook
* In the UK from `Chesterfield Model Making & Miniature Electronics <https://chesterfield-models.co.uk/product/semify-dcc-ex-motor-shield/>`_
* and other manufacturers licensed by DCC-EX.

The EX-CSB1 Command Stations come with an OLED status display and a carrier base mount (sometimes called a "sled" ) There are different options for the board such as with or without an additional EX-MotorShield 8874 for two additional DCC/PWM DC outputs. Prices vary from around $105-$145 in the US, to approximately £ XXX -fnd in the UK, € XXX -fnd in Europe, and in Australia starting from $AU175 -fnd. Prices typically do not include tax and shipping.

Ordering in Quantity or wishing to Resell
==========================================

For quantities of 10 or less per annum, you may utilise a PCB manufacturing and assembly service such as JLCPCB without licensing fees. A donation to DCC-EX would be appreciated, so click the DONATE button! The production files are available on the `DCC-EX GitHub <https://github.com/DCC-EX/EX-Motorshield8874>`_. XXX

Entrepreneurs wanting to use the design to offer commercial quantities to their local communities should contact DCC-EX (sales @ dcc-ex.com) to arrange a bulk purchase or a license to manufacture. Licensing includes donating a royalty to DCC-EX per board sold.

Board layout
==============

  * Input Power
  * Track A and B outputs
  * I2C connector
  * Railsync connector
  * Oled Header
  * GPIO Headers
  * Dual I2C Pin Header
  * Reset button
  * Motor Controller Chips - Hot area!
  * ESP32 Microprocessor
  * Antenna
  * Unpopulated power pads - Just because you are going to ask. For possible future use.
  * Board labels

Powering the EX-CSB1
=====================

The CSB1 has a standard 2.1mm x 5.5mm power jack, which makes connecting your power supply simple. If you already have a power supply with bare wires, you can use an optional 2.1mm x 5.5mm screw terminal block adapter. For more details on power supplies, check out our recommended power supplies section [link].

To power up the CSB1, just plug your power supply into the mains and connect the barrel end to the Command Station. Make sure your power supply matches the needs of your setup: the voltage should be between 12V and 25V DC, depending on the scale of your locomotives, and it should provide at least 4A of current. To get the most out of your EX-CSB1, we suggest using a power supply with 6A or more. For Z scale, 12V is usually enough, but for N, HO, and OO scales, we recommend using between 14V and 16V DC. It’s important that your DC power input is well-regulated—ideally, a modern switch-mode power supply with double insulation and strong overload protection.

Don’t worry if your power supply offers more amps than you need. While too much voltage can be harmful, extra current isn’t a problem since the CSB1 will only use as much as it needs. In fact, it’s better to have a bit more current than too little. However, remember that both voltage and current can be dangerous if not handled properly. The barrel connector helps add some safety, but be cautious—if, for example, a metal tool accidentally touches the terminals of a high-powered supply, it could cause a short circuit.

For more details on how much current you need, see [link].

When you connect power to the CSB1, you should see a bright green power LED light up, confirming that the electronics are working. However, for safety, track power will be off by default when you first plug in the EX-CSB1. This is to prevent power from accidentally being applied to your layout before everything is ready. If you prefer, you can change this default setting [link].

Connecting to Your tracks
==========================

Before connecting any wires to your tracks, make sure you unplug the power supply from the wall or remove the barrel connector from the command station. It's crucial to ensure that the command station has no power while you're working on your connections.

Once you're certain the power is off and the power LED is no longer lit, you can connect the wires from the A output (+ and -) to the track. For DCC operation, it doesn’t matter which wire goes to which rail, since there’s no polarity. However, as your layout grows, it’s important to stay consistent with your wiring to ensure that different power districts remain in phase. This simply means that as the tracks rapidly switch between positive and negative, all districts should stay synchronized. You can find more details about this in our wiring section [link].

For DC operation, polarity does matter. One rail is positive, and the other is negative, which determines the direction your train will move when voltage is applied through the command station. If you reverse the voltage, the train will change direction and run in reverse.


DCC Operation
=====================

The EX-CSB1 is set to operate in DCC mode by default. If you want to switch to DC mode, you can find instructions on how to do that [here].

Track Outputs
You’ll notice that the track outputs on the EX-CSB1 are labeled A and B. In standard DCC operation, output A is typically used for your MAIN track, where your trains run, and output B is for your PROG (Programming) track, where you can program and test your locomotives without affecting the main layout. However, with the flexibility of the EX-CommandStation software, you can configure any track to be a MAIN, PROG, DCC, DC, or even a Booster track. But don’t worry about that complexity for now—we’ll keep it simple.

DCC vs. DC: A Quick Overview
DCC (Digital Command Control): DCC uses a constant voltage on the track with digital signals embedded in the power to control the speed, direction, and functions of your trains. There’s no need to worry about polarity in DCC, making wiring simpler as your layout expands. The digital signal allows for precise control of multiple trains on the same track, all receiving power at the same time.

DC (Direct Current): DC operation is more traditional, where the direction and speed of your trains are controlled by varying the voltage and switching polarity. In DC mode, one rail is positive, and the other is negative. The train moves forward when voltage is applied and reverses direction when the polarity is flipped. DC control is simpler but less flexible, especially if you want to run multiple trains on the same track simultaneously.

Managing DCC and DC Modes in TrackManager
If you're ready to dive into customizing your track outputs, TrackManager is the tool you'll use. It allows you to easily switch between DCC and DC modes for any track connected to your EX-CSB1. You can also set up different tracks for specific purposes, such as making one track a Booster or configuring your PROG track.

For detailed steps on how to use TrackManager to change track modes and settings, check out the TrackManager help section [here].

DC Operation
===============

When using DC mode with the EX-CSB1, it's important to understand that this is not the traditional method of varying the DC voltage to control the speed of your locomotive. Instead, the track always receives full voltage whenever the throttle is set above zero. The speed of your train is controlled using a method called PWM (Pulse Width Modulation).

How PWM Works
PWM works by rapidly turning the voltage on and off to the track. The rate at which this happens adjusts the "effective" voltage that the locomotive's motor experiences. For example, if the voltage is on 50% of the time and off 50% of the time, the motor behaves as if it's receiving half of the full voltage. This technique is similar to how a DCC decoder controls a motor in a DCC-equipped locomotive.

Benefits of PWM in DC Operation
Using PWM for speed control has several advantages, particularly in terms of smooth operation. Trains start and stop more gradually, and running at slow speeds becomes smoother and more consistent. This gives you better control over your locomotives, making your layout more enjoyable to operate, especially during more delicate maneuvers.

USB Connection to install the Command Station Software
======================================================

The EX-CSB1 comes preloaded with the Command Station software, so you can start using it right out of the box. However, if you wish to customize its configuration or update the software, you can easily do so by connecting the EX-CSB1 to your computer via USB. Follow these steps to make any changes you need:

Step 1: Connect the EX-CSB1 to Your Computer
Locate the USB Port: Find the USB port on your EX-CSB1. It’s typically a USB-C port, depending on your model.
Use a Compatible USB Cable: Grab a USB cable that matches the port on your EX-CSB1. This will likely be a USB-A to micro-USB or USB-C cable.
Plug It In: Connect one end of the USB cable to the EX-CSB1 and the other end to an available USB port on your computer.

Step 2: Install the Required Drivers
Automatic Installation: In many cases, your computer will automatically recognize the EX-CSB1 and install the necessary drivers.
Manual Installation: If the drivers do not install automatically, you may need to download them from the official website. Follow the instructions provided on the site to complete the installation.

Step 3: Access or Update the Command Station Software
Open the Software: Since the EX-CSB1 comes preloaded with the Command Station software, you can access it directly by launching the program on your computer after connecting the EX-CSB1.
Download the Latest Version (Optional): If you want to update to the latest software version, visit the official DCC-EX website and download it. Open the installer and follow the on-screen instructions.
Modify the Configuration: The software allows you to customize the EX-CSB1’s configuration to suit your specific needs. Use the setup wizard or manual settings within the software to make any changes.

Step 4: Verify the Connection
Open the Command Station Software: Once the software is updated or if you’re making adjustments, launch it from your desktop or start menu.
Check the Connection: The software should automatically detect the EX-CSB1. If it doesn’t, ensure that your USB cable is securely connected and try again.

Step 5: Start Using or Customizing Your Command Station
With the EX-CSB1 connected, you’re ready to start using it or making any necessary adjustments to the configuration. Explore the features and tailor the settings to optimize your model railway experience.

Resetting the CS
=================

If you need to reset your EX-CSB1 Command Station software to its default settings, you'll need to reinstall the software. This process will overwrite your current configuration with the original default settings. Follow these steps to reset the software:

Step 1: Disconnect Power
Before you begin, make sure the Command Station is powered off. Unplug the power supply from the wall or disconnect the barrel connector from the CSB1. This ensures that the system is completely powered down before the reset process.

Step 2: Connect to Your Computer via USB
Locate the USB Port: Find the USB port on your EX-CSB1.
Use a Compatible USB Cable: Connect the CSB1 to your computer using the appropriate USB cable.
Power On: Plug the power supply back in or reconnect the barrel connector to power on the CSB1.

Step 3: Download the Latest Installer
Visit the DCC-EX Website: Go to the official DCC-EX website and download the latest version of the Command Station software installer.
Save the Installer: Save the installer file to a location on your computer where you can easily access it.

Step 4: Run the Installer
Open the Installer: Locate the downloaded installer file on your computer and double-click to run it.
Follow the On-Screen Instructions: The installer will guide you through the reinstallation process. During this process, the existing software on the EX-CSB1 will be overwritten with the default settings.
Complete the Installation: Allow the installer to complete the process. Once done, the software will be reset to its original configuration.

Step 5: Verify the Reset
Launch the Command Station Software: After the installation is complete, open the Command Station software to ensure it’s running correctly with the default settings.
Check the Configuration: Confirm that the software has been reset by checking the basic settings and making sure they match the defaults.

Step 6: Reconfigure if Necessary
Customize Settings: If you need to adjust the settings to suit your layout, you can now do so within the software.
Test Your Setup: Power up your layout and test the system to ensure everything is working as expected.



USB Connection to a Serial Monitor
===================================

Connecting your EX-CSB1 Command Station to a serial monitor is useful for debugging, monitoring operations, or making advanced configurations. The DCC-EX installer conveniently includes a built-in serial monitor, making it easy to get started. Here’s how to set up this connection:

Step 1: Connect the EX-CSB1 to Your Computer
Locate the USB Port: Find the USB port on your EX-CSB1, which is typically a USB-C port.
Use a Compatible USB Cable: Connect the EX-CSB1 to your computer using a suitable USB cable (USB-A to micro-USB or USB-C, depending on your EX-CSB1 model).
Power On the Command Station: Ensure the Command Station is powered on by connecting the power supply. The green power LED should be lit.

Step 2: Install Required Drivers
Automatic Driver Installation: Most modern operating systems will automatically detect the EX-CSB1 and install the necessary drivers when you connect it via USB.
Manual Driver Installation: If the drivers do not install automatically, you can download them from the official DCC-EX website and follow the provided instructions.
Step 3: Open the Serial Monitor
Use the DCC-EX Built-in Serial Monitor: The DCC-EX installer includes a built-in serial monitor, which simplifies the process. To access it, launch the DCC-EX software on your computer.
Select the Correct Port: In the built-in serial monitor, select the COM port that corresponds to the EX-CSB1. This is usually labeled something like “COM3” or “ttyUSB0” depending on your operating system.
Set the Baud Rate: Configure the serial monitor to the correct baud rate. The typical baud rate for the EX-CSB1 is 115200. This setting ensures that data is transmitted at the correct speed between the Command Station and your computer.

Step 4: Monitor Serial Output
Open the Connection: Once the correct port and baud rate are selected, open the connection in the serial monitor.
View Output: You should begin to see data streaming from the EX-CSB1. This might include diagnostic information, feedback from commands, or other operational details depending on your setup.

Step 5: Send Commands (Optional)
Input Commands: If you need to send commands to the EX-CSB1, you can do so by typing them directly into the serial monitor input field and pressing enter.
Observe Responses: Watch the serial monitor for responses to your commands, which can help with troubleshooting or advanced configurations.

Step 6: Close the Connection
Safely Disconnect: When you’re done, close the connection in the serial monitor and safely disconnect the USB cable from your EX-CSB1.
Power Down (if needed): If you need to power down the Command Station, unplug the power supply or disconnect the barrel connector.

USB Connection to JMRI
=======================

Connecting your EX-CSB1 Command Station to JMRI (Java Model Railroad Interface) via USB allows you to control your model railroad layout using a comprehensive suite of tools. Follow these steps to set up the connection:

Step 1: Connect the EX-CSB1 to Your Computer
Locate the USB-C Port: Find the USB-C port on your EX-CSB1.
Use a Compatible USB-C Cable: Connect the EX-CSB1 to your computer using a USB-C cable.
Power On the Command Station: Ensure the Command Station is powered on by connecting the power supply. The green power LED should be lit.

Step 2: Install Required Drivers
Automatic Driver Installation: Most modern operating systems will automatically detect the EX-CSB1 and install the necessary drivers when you connect it via USB-C.
Manual Driver Installation: If the drivers do not install automatically, download them from the official DCC-EX website and follow the provided instructions.

Step 3: Install and Set Up JMRI
Download and Install JMRI: Visit the official JMRI website and download the latest version of the software. Follow the installation instructions to set it up on your computer.
Launch JMRI: Once installed, open JMRI. You’ll typically start with either DecoderPro or PanelPro, depending on your needs.

Step 4: Configure JMRI for EX-CSB1
Go to Preferences: In JMRI, navigate to Edit > Preferences.
Select System Connection: Under the "Connections" tab, choose "DCC++EX" (or "DCC++" if that’s the available option) as your system manufacturer.
Choose USB Port: For the connection type, select "Serial" or "USB." Then, choose the correct COM port that corresponds to your EX-CSB1. This is usually labeled something like “COM3” or “ttyUSB0” depending on your operating system.
Set Baud Rate: Ensure the baud rate is set to 115200, which is the standard for EX-CSB1 communication.
Save and Restart: After configuring these settings, save them and restart JMRI to apply the changes.

Step 5: Verify the Connection
Test the Connection: After JMRI restarts, it should automatically connect to your EX-CSB1. You can verify this by checking the status in the JMRI window.
Control Your Layout: Begin using JMRI’s tools to control your trains, turnouts, and other layout elements. You should now have full access to JMRI’s capabilities through your EX-CSB1.

Step 6: Troubleshooting (if needed)
Check Connections: If the connection fails, ensure that the USB-C cable is securely connected and that the correct COM port is selected.
Reinstall Drivers: If issues persist, you may need to reinstall the drivers or update JMRI to the latest version.
Consult Documentation: Refer to the JMRI or DCC-EX documentation for additional troubleshooting steps.

Integrated displays
====================

The EX-CSB1 Command Station supports integrated displays, providing a convenient way to view system information, monitor operations, and interact with your layout directly from the device. Here’s how to set up and use integrated displays with your EX-CSB1:

Step 1: Choose a Compatible Display
Display Type: The EX-CSB1 is compatible with a variety of integrated displays, such as OLED or LCD screens. These displays typically connect via I2C interfaces.
Size and Resolution: Select a display size and resolution that meets your needs. Common sizes include 0.96-inch to 2.4-inch displays with resolutions suitable for displaying clear text and simple graphics.
Purchase the Display: Ensure that you purchase a display that is compatible with your EX-CSB1. If in doubt, check the DCC-EX documentation or website for recommended models.

Step 2: Connect the Display to the EX-CSB1
Locate the I2C Display Port: On the EX-CSB1, there are dedicated I2C connection points labeled as "OLED I2C" and "I2C x 2" on the board.

Wiring the Display:

For I2C Displays: Connect the SDA (Data) and SCL (Clock) pins on the display to the corresponding SDA and SCL pins on either the "OLED I2C" or "I2C x 2" connectors on the EX-CSB1.
OLED I2C: Use this for directly connecting an OLED display.
I2C x 2: This can be used for connecting other I2C devices or displays that require separate I2C connections.
Power Connections: Connect the VCC (power) pin of your display to the 3.3V or 5V pin on the EX-CSB1, depending on the power requirements of your display. The ground (GND) pin of the display should be connected to the GND pin on the EX-CSB1.
Power On the Command Station: After wiring the display, power on the EX-CSB1. The display should initialize, showing basic startup information.

Step 3: Configure the Display Using the DCC-EX Installer
Open the DCC-EX Installer: Launch the DCC-EX installer software on your computer. This software will guide you through configuring the display settings.
Access Display Configuration: Within the installer, navigate to the display configuration section.
Select the Display Type: Choose the type of display you have connected (I2C) and specify any additional settings such as the address for I2C displays.
Customize Display Output: You can customize what is shown on the display, such as system status, track voltage, throttle settings, and more. Follow the on-screen instructions within the DCC-EX installer to set up your preferred layout.
Save and Apply Settings: Once you’ve configured the display settings, save your changes and apply them. The display should now show the configured information.

Step 4: Using the Integrated Display
Monitor System Status: The display can show real-time system information such as current track voltage, train speed, or error messages. This allows you to keep an eye on your layout without needing to check the computer.
Update Information: The display will automatically update as the system operates, providing you with the latest data on your layout’s performance.

Step 5: Troubleshooting Display Issues
Check Connections: If the display does not turn on or show the correct information, double-check the wiring and ensure all connections are secure.
Verify Software Settings: Ensure that the display type and configuration settings in the DCC-EX installer match the actual setup.
Consult Documentation: Refer to the display’s datasheet or the EX-CSB1 documentation for additional troubleshooting tips.

Connecting Accessories (I2C)
=============================

The EX-CSB1 Command Station allows you to expand your model railway setup by connecting various I2C accessories such as sensors, displays, and GPIO expanders. Using the DCC-EX Installer and additional tools, you can easily configure these accessories to work with your layout.

Step 1: Selecting I2C Accessories
Choose Compatible Accessories:
Common I2C accessories include displays (e.g., OLED, LCD), sensors (e.g., temperature, distance), and GPIO expanders.
Ensure your accessories are compatible with I2C and check the DCC-EX website for supported devices.

Step 2: Connecting Accessories to EX-CSB1
Locate the I2C Ports:
Use the "I2C x 2" ports for general I2C devices.
Use the "OLED I2C" port if you're connecting an OLED display.
Wiring the Devices:
SDA (Data Line): Connect the SDA pin on your accessory to the SDA pin on the EX-CSB1.
SCL (Clock Line): Connect the SCL pin on your accessory to the SCL pin on the EX-CSB1.
Power: Depending on your device’s requirements, connect the VCC pin to either 3.3V or 5V on the EX-CSB1. Connect the GND pin to GND.
Daisy-Chaining Multiple Devices: If connecting more than one I2C device, ensure each has a unique I2C address, which can be set via jumpers or configuration switches.

Step 3: Installing and Running the DCC-EX Installer
Download and Install:

Visit the DCC-EX Installer page to download the latest version.
Follow the on-screen instructions to install the software on your computer.
Run the Installer:

Connect your EX-CSB1 to your computer via USB.
Open the DCC-EX Installer. The installer will guide you through the initial setup, including basic configurations like setting up I2C displays.
Configuring I2C Displays:

The installer will allow you to configure connected displays (such as OLED or LCD) directly during the setup process.
For other I2C devices, further configuration may require manual adjustments using the DCC-EX CommandStation software or editing configuration files.

Step 4: Manual Configuration for Advanced Accessories
Access the CommandStation Software:

For advanced I2C accessories like sensors or GPIO expanders, you may need to manually configure them via the DCC-EX CommandStation software.
This involves accessing configuration files or using a serial monitor to input specific commands.
Editing Configuration Files:

If necessary, open the configuration files provided with the DCC-EX software to manually add and configure your I2C devices. Instructions for this can be found on the DCC-EX documentation pages.
Save and Apply Settings:

After configuring your devices, ensure you save and apply your settings through the CommandStation software.
Step 5: Testing and Troubleshooting
Test Your Setup:

Once configured, power on your layout and check if the I2C devices are functioning correctly.
Use the diagnostics tools provided by the DCC-EX software to troubleshoot any issues.
Troubleshooting Common Issues:

Double-check wiring connections and I2C addresses.
If issues persist, refer to the troubleshooting guides on the DCC-EX website.
Additional Resources
For more detailed instructions and support, refer to these resources:

DCC-EX I2C Hardware Overview
Using the EX-CommandStation Software
DCC-EX Installer Guide
Connecting and Configuring I2C Displays