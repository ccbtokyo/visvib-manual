はい、Markdownの文章を英訳いたします。以下が翻訳です:

# Troubleshooting

## Application launch is blocked

On both Windows and macOS, when you first launch an application after downloading it, the security system may block its startup.

![Screenshot of a Windows dialog saying "SmartScreen can't be run right now". Buttons "Run" and "Don't run" are shown in the bottom right.](../img/windowsdefender1.png)

On Windows, if you're not connected to the internet, you'll see a dialog saying "SmartScreen can't be run right now". In this case, click "Run" to start the application.

![Screenshot of a dialog saying "Windows protected your PC". Only the "Don't run" button is shown in the bottom right. The phrase "More info" at the end of the dialog text is surrounded by an orange dotted line.](../img/windowsdefender2.png)

If you're connected to the internet, you'll see a dialog saying "Windows protected your PC", but if you click on "More info", a "Run" button will appear, allowing you to start the application.

![The same dialog as before, after clicking "More info". A new "Run" button has appeared in the bottom right.](../img/windowsdefender3.png)

On macOS, instead of double-clicking the application file in Finder or on the desktop, right-click and select "Open" from the menu. This method will make an option to launch the application appear in the dialog.

On both Windows and macOS, once you've launched the application once, you can start it normally like any other application afterwards.

## Audio application doesn't start

[Please check if Max is installed correctly.](./2-prep-software.md#installing-cycling-74-max)

## No sound response in the audio application

- Click "Audio Settings" in the application and check if the "INPUT DEVICES" in the menu of the window that appears shows the name of the audio interface you're using.
- Check if the "DSP" button is lit up green. If not, click it to start DSP.
- Make sure the pitch of the tone chime you're using matches the note name on the "Pitch" dial in the application.

## Sound information is not reflected in the lighting

First, check if the brightness of the lights changes when you drag the Light Brightness slider in the audio application.

### The brightness changes with the slider

The connection to the lighting equipment itself is not a problem. After confirming that "Output" in the "Range" section of the audio application is set to 255, try setting "Input" to a small value like 0.07 and see if there's a response.

### The brightness doesn't change even with the slider

There's a problem with the lighting equipment connection.

- Check if the LED next to the USB connector on the DMX USB PRO lights up when you move the slider. If there's no response, the audio program isn't recognizing the DMX USB PRO. Check if there are any other USB devices connected.
- Check if the LEDs on the dimmer side with numbers 1, 2, 3, 4 are lit. If not, either the DMX cable connection is not made or the channel settings are incorrect.
- If the dimmer side is receiving the signal but not lighting up, there might be a problem with the light itself. Check if you're using incandescent bulbs and if the power to the light fixture itself is on.

## Sound information is not reflected in the video

Check the following in the "Device Communication" of the audio application:

- Is the `LOCAL_MODE` button yellow? If not, click it.
- Check if the "port" number in the bottom right matches the port number in the video application.
    - By default, the communication port is set to 8888, but it may be conflicting with other applications. Try a few arbitrary numbers after 8000.
- The OS firewall settings may prevent proper communication between applications.
    - If necessary, temporarily turn off the firewall settings. (Note that this poses a security risk if you're connected to the internet.)