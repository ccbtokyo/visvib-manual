# Practical Use Part

First, let's start the
applications. [If the system blocks the launch when starting for the first time after downloading, ignore it and launch anyway.](../Troubleshooting/index.en.md#application-launch-is-blocked)

![Screenshot of Max application.]()

Double-clicking the Max project file named `ccbt_tonechime_sensor` in the audio program folder will launch the
application for audio analysis and lighting control in Max.

![Screenshot of video application.]()

Double-clicking the application named `Tonechime_VideoSystem` in the video application folder will launch the video
application. At this time, if an external display is connected, the video application will automatically display in full
screen. A small operation window will be displayed on the main display.

After launching the applications, first set up the audio interface and DMX connections.

![Audio settings window.]()

First, click the "Open Audio Setting" button in the top right. A new window will open. In the second item from the top,
DRIVER, select "ad_portaudio" or "Windows DirectSound" (or "Core Audio" for Mac). In the third item, INPUT DEVICE,
select the name of the audio interface you are using. After selecting, close the audio settings window.

If the "DSP" button is gray, click it to turn it green.

![Screenshot with DMX settings area circled]()

Click the DMX button below to turn it green as well. If the USB DMX PRO is connected, the icon to the right will light
up green and display "Connected".

> [!NOTE]
> The application automatically detects serial communication devices connected via USB. If multiple serial devices are
> connected, it may attempt to connect to devices other than the USB DMX PRO, so please do not connect USB devices
> unrelated to the system.

![Screenshot with OSC settings area circled]()

Click the "OSC" button below to turn it green, and also click "LOCAL_MODE" to turn it yellow.

> [!NOTE]
> Turning off "LOCAL_MODE" allows synchronization with a video application running on another computer. Enter the IP
> address of the computer running the video application in the address field next to port.

![Screenshot with save settings area circled]()

Press the "Save Config" button in the top right. If the configuration of connected devices is the same, the current
parameters, including audio interface settings, will be automatically restored the next time you launch the application.

> [!NOTE]
> Parameters are written in a file named `data/main.json`. You can also directly edit `pattrstorage/slots/1/data` in the
> JSON data.

## Setting Tone Chime Pitch and Volume

![Screenshot with pitch settings area circled]()

In the audio analysis program, we prevent detection of unnecessary noise by specifying the pitch of the tone chimes to
be used in advance. You can adjust the pitch and volume of the tone chimes at the bottom of the audio analysis app
screen.

Drag the dial labeled "Pitch" to match the name of the pitch of the tone chime you are using. Also, make sure the button
labeled BPF to the right is lit yellow.

> [!NOTE]
> In the software, the pitches of black keys are notated as `A#4` or `D#4`, but on tone chimes, they are notated as
> flats like `B♭4` or `E♭4`, so be careful not to confuse them.

Next, let's set the volume (sensitivity) of the contact microphone. When you strike the tone chime, the volume of the
sound is displayed in the meter in the part labeled gain.

![Photo of input knob area]()

Turn the input gain knob on the audio interface to the right until the meter does not turn red or yellow when you strike
the tone chime strongly.

If the peak overload lamp on the audio interface lights up, or if the volume is still low even after turning the knob
all the way up, drag the gain meter in the application to further adjust the volume.

When using multiple tone chimes, adjust the pitch and volume for all channels. Press "Save Config" again to save the
settings.

## Lighting and Video Settings

![Screenshot of light area]()

Let's set up the lighting. First, drag the Light Brightness slider left and right to check if the brightness of the
lights changes. If the brightness does not change when you move
this, [there should be a problem with the DMX and lighting connections or dimmer settings in the Setup section](../Troubleshooting/index.en.md#sound-information-is-not-reflected-in-the-lighting).

If the Light Brightness does not reach the far right when you strike the tone chime strongly, gradually lower the
Range-Input slider at the top.

In the video system, circles with colors set for each channel change their size according to the volume.

At this time, the video effect changes in three stages depending on the volume. You can set at what volume to divide
large, medium, and small using the High, Mid, and Low sliders in Detection Threshold.

In the Video section at the bottom of the app, you can see the actual volume change and the three-stage division
positions, so try striking with different volumes to find good division points.

In the video application, you can set the color for each channel.

If the lights flicker finely even when no sound is actually playing, increase the value of the Smoothing slider.

Similarly, if there are fine reactions in the video, try increasing the attack slider in Detection Threshold.

![Screenshot of smoothing-related area]()

Before closing the application, press Save Config again when it is working well.

You can close the audio application with the ❌ button in the top right (top left for macOS). The settings of the video
application are saved automatically. Click the exit button in the bottom right to close.

> [!WARNING]
> For the video application, the information will not be saved unless you exit using the exit button in the bottom
> right. Do not exit using the ❌ button on the window.