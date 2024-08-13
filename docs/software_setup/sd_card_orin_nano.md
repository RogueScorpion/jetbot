# Software Setup (SD Card Image)

This page details how to set up JetBot using the pre-built JetBot SD card image. You may prefer this option if you are new to Jetson Orin Nano, and do not have an existing SD card configured.


## Step 1 - Initial Setup Guide for Jetson Orin Nano

This [link](https://www.jetson-ai-lab.com/initial_setup_jon.html) contains details about the initial setup. Most likely, you made need to flash Jetpack 5.x first and then upgrade to 6.x. The specified link contains details of the process.


## Step 2 - Setup Jetbot through Docker

1. Insert an SD card into your desktop machine





## Step 4 - Connect JetBot to WiFi

Next you'll need to connect to WiFi.  To reduce memory consumption, we disable the Ubuntu GUI in the latest JetBot SD card image.  For this reason, you'll need to use the command line to connect to WiFi.

1. Log in using the user ``jetbot`` and password ``jetbot``
    
2. Connect to a WiFi network using the following command

    ```bash
    sudo nmcli device wifi connect <SSID> password <PASSWORD>
    ```
    
Your Jetson Nano should now automatically connect to the WiFi at boot and display it's IP address on the piOLED display.

???+ tip
    If you're having trouble figuring out how to get connected to Wi-Fi, check out the [Wi-Fi setup](wifi_setup.md) page for more detailed instructions 

## Step 5 - Connect to JetBot from web browser

After your robot is connected to WiFi, you no longer need to have the robot connected by a monitor.  You can connect to the robot from your laptop's web browser by performing the following steps

1. Shutdown JetBot using the command line

    ```bash
    sudo shutdown now
    ```

2. Unplug your HDMI monitor, USB keyboard, mouse and power supply from Jetson Nano

3. Power the JetBot from the USB battery pack by plugging in the micro-USB cable
4. Wait a bit for JetBot to boot
2. Check the IP address of your robot on the *piOLED* display screen.  Enter this in place of ``<jetbot_ip_address>`` in the next command
3. Navigate to ``http://<jetbot_ip_address>:8888`` from your desktop's web browser. You can do this from any machine on your local network.  
4. Sign in using the password ``jetbot``.

That's it, you've now accessed JetBot's remote programming environment! 

You will be presented with a view similar to the following. 

![](../images/docker_jupyter-on-browser.png)

Here you can easily access the JetBot examples!  From this point on, when you power on the JetBot, it should automatically connect to WiFi and display it's IP address.  So all you need to do is reconnect using your web browser to start programming!

Now that you're finished setting up your JetBot, you're ready to run the [examples](../examples/basic_motion.md).
