# Preparation - Hardware Section

![Image of a completed setup with sensors attached to tone chimes.](../img/tonechime-complete.jpg)

In the VisVib system, vibration sensors (contact microphones) attached to tone chimes are analyzed on a computer and converted into lighting and video.

## Required Equipment by Configuration

The original configuration uses 8 tone chimes and sends information to the computer via wireless transmitter. However, as this setup is large-scale and expensive, this document presents three example configurations:

- 8 Tone Chimes with Wireless Connection
- 2 Tone Chimes with Wireless Connection
- 2 Tone Chimes with Wired Connection

| Category | Item | 8 Wireless | 2 Wireless | 2 Wired |
| :------: | ---- | :--------: | :--------: | :-----: |
| Instrument | Tone Chimes | 8 | 2 | 2 |
| PC | Computer | 1 | 1 | 1 |
| Video | Display or Projector | 1 | 1 | 1 |
|  | Video Connection Cable (e.g., HDMI) | 1 | 1 | 1 |
| Audio | Contact Microphones (Self-made) | 8 | 2 | 2 |
|  | Audio Transmitter | 4 | 1 | - |
|  | 3.5mm to 6.3mm Plug Converter | - | - | 2 |
|  | Audio Interface | [A](#a) | [B](#b) | [B](#b) |
| Lighting (Optional) | Dimmer Pack | 2 | 1 | 2 |
|  | Incandescent Bulbs | 8 | 2 | 2 |
|  | ENTEC DMX USB PRO | 1 | 1 | 1 |
|  | XLR Cable | 2 | 2 | 2 |
|  | XLRF3-M5 Pin Converter | 1 | 1 | 1 |

## Instrument

[SUZUKI Tone Chimes](https://www.suzuki-music.co.jp/products/36403/)

These are rod-shaped instruments similar to handbells. In the workshop, we use 8 notes selected from the middle-range basic set HB-250N. The 3D-printed attachment for attaching the microphone is compatible with the two sizes in this basic set.

### Contact Microphone

![Image of custom microphones. On the left is a version with a cover, on the right is a version without a cover.](../img/microphone.JPG)

We use custom-made contact microphones. These microphones pick up vibrations directly from the object they're attached to, rather than air vibrations.

These microphones can be easily made by soldering an inexpensive component called a piezo element to a cable.

For instructions on how to make the microphone, please refer to the document **[1-1 How to Make a Microphone](./1-1-make-contact-microphone.md)**.

A dedicated cover for the microphone can be 3D printed. This is optional and not necessary for operation.

![Screenshot of the 3D model of the cover.](../img/cover_3dmodel.png)

![Photo of the cover right after 3D printing, with support material still attached.](../img/3dprint_image.jpg)

The 3D model data for printing can be downloaded from the following links:

|     | Main Cover | Cable Clip |
|:---:| :--------: | :--------: |
| Large | [piezo_cover_large.stl](../3dmodels/piezo_cover_large.stl) | [cableclip_large.stl](../3dmodels/cableclip_large.stl) |
| Small | [piezo_cover_small.stl](../3dmodels/piezo_cover_small.stl) | [cableclip_small.stl](../3dmodels/cableclip_small.stl) |

## PC and Video Equipment

- Computer

This document assumes a Windows environment, but it can also work in a macOS environment.

Memory: 8GB
OS: Windows 10 or later / macOS 13 (Ventura) or later

- Display or Projector and Screen (any model)
- Cable to connect display to computer (e.g., HDMI) x1

## Audio Equipment

## Audio Interface

This is a device for inputting sound from the microphone into the computer.

### A

[MOTU UltraLite Mk5](https://www.soundhouse.co.jp/products/detail/item/291119/)

Other models such as RME FireFace UFX can be used if they have 8 or more line inputs available.

### B

[Roland Rubix24](https://www.roland.com/jp/products/rubix24/)

If you already have A, you can use it without any issues.

## Audio Transmitter (for wireless connection)

[SENNHEISER EW 122P G4-JB](https://www.soundhouse.co.jp/products/detail/item/254766/)

The EW112P is also fine. We've chosen this transmitter because it can use up to 8 units simultaneously. For configurations with fewer channels, a less expensive option would also work. Be careful of wireless channel interference with other B-band devices at the venue.

Bluetooth or other transmitters can be used, but there may be latency issues.

## Lighting Equipment

### Dimmer

![Close-up image of the dimmer.](../img/dimmerpack.jpg)

[AMERICAN DJ / DP415R](https://www.soundhouse.co.jp/products/detail/item/252223/)

- A device that controls AC100V outlet voltage using DMX signals.
- Other alternatives include Elation Cyber Pak or LITE-PUTER DX-402A.
- Each unit can control up to 4 channels, so 2 units are needed if using more than 5 lights.

### DMX-USB Converter

![Close-up image of DMX USB PRO](../img/dmxusbpro.jpg)

[ENTEC DMX USB PRO](https://www.enttec.com/product/dmx-usb-interfaces/dmx-usb-pro-professional-1u-usb-to-dmx512-converter/)
  - A converter adapter for controlling DMX signals from a computer via USB.

Additionally, prepare the following cables and converter adapters:

- XLR cable: The same 3-pin audio type is fine. Length as needed.
- XLR Female 3-pin to XLR 5-pin Male converter adapter
  - Such as [NEUTRIK NA3F5M](https://www.soundhouse.co.jp/products/detail/item/236711/).

### Incandescent Bulbs

Any incandescent bulb that plugs into a regular outlet, such as clip lights, will do. However, do not use fluorescent or LED bulbs as a rule. While dimmable ones can be used, they are not recommended as they completely turn off below a certain brightness level.