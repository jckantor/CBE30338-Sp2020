# Updating TCLab Firmware

The Temperature Control Lab is implemented with an Arduino microcontroller. Custom firmware in the form of standard Arduino sketch is installed on the Arduino to facilitate two-way with the host laptop via a USB cable. These are the instructions to  install and update the Temperature Control Lab firmware.

### 1. Download the Arduino IDE

The Arduino IDE is an Arduino development environment used to code and operate Arduino devices. Download the latest version for your laptop from this link [https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software). (A contribution is not required to download and install the software.)

The application may run right out of the downloads folder without requiring further installation steps. This is convenient if you plan to discard the application after you're done with this update.

### 2. Connect the TCLab hardware

Use the USB cable provided with the TCLab kit to connect the TCLab hardware to your laptop. (You will need to provide a USB-A to USB-C adapter if your laptop has only USB-C ports.) One more LED's will light up on the Arduino board after connection.

Next open the Arduino IDE application. Ihere may be confirmation screens to go through if this your first time with the application. Once open, click on the `Tools` menu, then look under the `Board` submenu to select `Arduino Leonardo`. This should match the model name on the back of your Arduino board.

Click again on the `Tools` menu and look under the `Port` submenu. There may be several entries depending your laptop and other accessories that you may be using. The exact name will depend on your laptop. Select the one that specifies a link to the Arduino. 

### 3. Download TCLab-sketch.ino from the Github repository

Download `TCLab-sketch.ino` from the [TCLab-sketch repository on Github](https://github.com/jckantor/TCLab-sketch/tree/master/TCLab-sketch). To download, click on the file name on Github to open the file listing, then click on the button just above the file header labeled `Raw`. A plain text listing will appear in your browser window. From there, use the browser's file menu to save the page to your laptop. Some laptop/browser combinations will add a `.txt` suffix to the filename during the download. If this happens to you, rename the file to remove the `.txt`.  When finished the filename on your laptop should appear as `TCLab-sketch.ino`.

### 4. Upload the TCLab-sketch.ino using the Ardunio IDE

Use the Arduino IDE file menu to open the `TCLab-sketch.ino` file that you downloaded. The application may ask permission to create a new folder and to move the file to that folder. If so, click `OK`. At this point an edit window should be open in the Arduino IDE displaying the contents of`TCLab-sketch.ino`. 

Under the `Sketch` menu, select `Verify/Compile`. You should  get a message at the bottom of the edit window indicating success. If you encounter errors at this step, confirm that that file displayed in the Arduino IDE edit window is exactly the same as it appears in the Github repository.

Next, from the `Sketch` menu select `Upload`.  This will take a few seconds to complete. At this point you are finished with the firmware upload. You can close the Arduino IDE application. 

If you get `avrdude` errors there may be a problem with your laptop communicating with the Arduino hardware. Here are some things that have helped in these circumstanaces:

* If you are working on a Mac, check the `Ports` submenu again. If there is no entry obviously associated with the Arduino, then reboot your Mac with the Arduino connected by USB. This will provide your Mac with an opportunity to recognize the device and to download an appropriate device driver during the restart.
* If you are working on Linux, try logging in as root or superuser to give the Arduino IDE permission to access your computer hardware.

### 5. Verify

Use one of the existing notebooks to test your connection to the Temperature Control Lab. 

