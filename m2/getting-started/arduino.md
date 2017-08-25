# Arduino IDE Quick Start

By completing this guide you will configure the Arduino IDE for developing on the Macchina M2 and run your first sketch on the M2.  This will verify both your Arduino IDE setup and your M2 device.

The following steps are needed to get started programming on the Macchina M2 with the Arduino IDE:

1. Install the Arduino Desktop IDE
2. Install the Macchina M2 Board Configuration
3. Install drivers
4. Build and upload a sketch

## Arduino Desktop IDE

Follow the official installation instructions for your operating system then return here to continue with Macchina M2 specific setup.

- [Windows](https://www.arduino.cc/en/Guide/Windows)
- [macOS](https://www.arduino.cc/en/Guide/MacOSX)
- [Linux](https://www.arduino.cc/en/Guide/Linux)

## Macchina M2 Board Configuration

Now that you have the Arduino IDE Installed, you will add support for the for _Macchina M2_.

First, you will tell the IDE where to find the Macchina board configuration files.  Go to **_File_** > **_Preferences_**.  Paste

    https://macchina.cc/package_macchina_index.json 

into the **_Additional Board Manager URLs:_** box and press **_OK_**.  This tells the Arduino IDE where to look to find the board configuration files for Macchina boards.

Next, you will open the **Boards Manager** to download the needed board configurations.  Find the board manager under **_Tools_** > **_Board: "[...]"_** > **_Boards Manager.._**.

In the board manager, install **Arduino SAM Boards (32-bit ARM Cortex-M3) by Arduino**.  Then install **Macchina SAM Boards (Install Arduino SAM Boards first) by Macchina**.

## Drivers

You may need to install a driver to enable your computer to communicate with the Macchina M2 before you can send sketches to it.  The Macchina M2 is based on the Arduino Due and uses the same driver.  Please visit the official Arduino Due documentation for [instructions on installing drivers](https://www.arduino.cc/en/Guide/ArduinoDue#toc4).

Be careful when plugging the micro-USB cable into your M2.  The M2's design allows you to put it in a case or enclosure.  The connector cable may stick out farther than you expect, because there needs to be clearance space for a case.

When you have finished installing drivers, leave your Macchina M2 plugged into the computer.

## Running your first sketch

Now that you have the Arduino IDE setup and your M2 connected, you can run your first sketch on the M2 by performing the followings steps in the Arduino IDE.

First, you will make **Macchina M2** the active board.  **_Tools_** > **_Board: "[...]"_** > **_Macchina M2_**.

Next, open the Blink sketch. **_File_** > **_Examples_** > **_01. Basics_** > **_Blink_**.

Finally, in the opened window, upload the sketch to your M2 board.  **_Sketch_** > **_Upload_**.

It will take a few moments for the sketch to be written as firmware to your Macchina M2.  You can watch the progress at the bottom of the IDE window.  When the upload has completed, you should see a flashing LED on your Macchina M2.

Congratulations!  You have now configured your computer for development on the M2 and run your first program.  As a next step, you may choose to learn the names of the other LEDs on the Macchina M2 using the [pin mapping](/m2/processor/pin-mapping).  Then you can practice modifying the sketch to make other LEDs blink.