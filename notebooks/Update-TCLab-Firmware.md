# Updating TCLab Firmware

The Temperature Control Lab has been implemented with an Arduino microcontroller. Custom firmware in the form of standard Arduino sketch has been written and installed on the Arduino to facilitate two-way with the host laptop via a USB cable. From time-to-time it may be necessary to install updates to the firmware. These are the instructions for installing firmware updates.

### 1. Download the Arduino IDE

The Arduino IDE is an Arduino development environment used to code and operate Arduino devices. Download the latest version for your laptop from this link [https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software). (Please note that a contribution isn't required to download and install the software.)

Note that the application may run right out of the downloads folder without further installation which is convenient if you plan to discard the application after you're done with this update.

### 2. Connect the TCLab hardware

Use the provided USB cable to connect the TCLab hardware to your laptop. (You will need to provide a USB-A to USB-C adapter if your laptop has only USB-C ports.) You should see one more LED's lit on the Arduino board.

Once connected, open the Arduino IDE application. If this your first time with the application, there may be confirmation screens to go through.

Once the application is open, click on the `Tools` menu, look under the `Board` submenu, and select the `Arduino Leonardo` option. This should match the model name on the back of your Arduino board.

Click again on the `Tools` menu and look under the `Port` submenu. There may be several entries depending your laptop and other accessories that you may be using. Select the one that specifies a link to the Arduino.

### 3. Download TCLab-sketch.ino from the Github repository

Download `TCLab-sketch.ino` from the [TCLab-sketch repository on Github](https://github.com/jckantor/TCLab-sketch/tree/master/TCLab-sketch). To download, click on the file name on Github. When you see the actual file listing, click on the button just above the file header labeled `Raw`. The file listing should now appear as plain text in your browser window. From there, use the browser's file menu to save the page to your laptop. Please note that some laptop/browser combinations will add a `.txt` suffix to filename after download. If this happens to you, rename the file to remove the `.txt`.  When finished, the filename on your laptop should appear as `TCLab-sketch.ino`.

### 4. Upload the TCLab-sketch.ino using the Ardunio IDE

Then use the Arduino IDE file menu to open the `TCLab-sketch.ino` that you downloaded above. The application may ask permission to create a new folder and to move the file to that folder. If so, click `OK`. At this point an edit window should be open in the Arduino IDE displaying the contents of`TCLab-sketch.ino`. 

Under the `Sketch` menu, select `Verify/Compile`. You should quickly get a message at the bottom of the edit window indicating it is done compiling.

Next, under the `Sketch` menu, select `Upload`.  This will take a few seconds to complete after which you will get a `Done uploading` message. At this point you are finished with the firmware upload. You can close the Arduino IDE application.

### 5. Verify

Use one of the existing notebooks to test your connection to the Temperature Control Lab. 


