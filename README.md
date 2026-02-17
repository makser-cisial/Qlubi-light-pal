# Qlubi-light-pal

A desktop buddy who’s there to connect when you feel most alone

Qlubi is a networked companion device that converts heart rate stress signals into anonymous light communication, enabling trusted groups to support each other remotely through subtle, non-verbal interaction.


---

## What it is

Qlubi network-based device designed to connect groups working and living separately and provide accompaniment through its communicative light system. Composed of a microcontroller, button, LED strip, and limited 3D printed parts, the device allows user to create a network by which they can pick up on and engage with each other’s distress without surveillance or intrusion.

The project is open source and designed to be customised and built upon, turning each Qlubi into someone’s made to be buddy.


Watch the product video at: https://www.youtube.com/watch?v=_jfL0hginCQ
---

## Concept

Today’s world provides a uniquely extreme environment in the way that it has pushed social connection to its limit. No longer can one pick up on the body language of a colleague in the office to see they may be stressed and need a hand or a knowing glance. No one is there to notice when someone is stressed, so much so the person themselves doesn’t realise it either without the outside prodding of others. 

Qlubi exists to fill that space, bringing these non-verbal forms of communication and connection to the digital world. By syncing one’s heart rate data with the device, users can create trusted networks with friends where when one’s heart rate rises from stress, and an anonymous signal is sent throughout the network, allowing others to interact with their devices to send back heartening signals through warm waves of pulsating light.

---

## Key Questions

### Who’s connected?

Users can form intentional networks of devices with whoever they please, connecting through personal servers via MQTT protocol meaning you're only connected to those you know and trust.

### What travels through the network?

Only anonymised messages that shift the states of the devices as all heart rate data is processed locally keeping one’s data private and secure. You don’t know who’s stress you’re responding to or what may be stressing them out allowing outreach without exposure and support without interference.

### How come light?

Light allows for a soothing and non-jarring means of communication when compared to sound, allowing it to only just catch the users attention and alert them out of their stress cycle without activating any further stress response. Being light based also allows the device to function in public spaces without disturbing those near which also contributes to a more intimate and deliberate experience as you know someone out there is paying attention to your call.

### How does one interact with the device?

When receiving signals, users can pat their Qlubi’s head, pressing the internal button and thus responding and interacting with the network, turning what would have been cold keyboard clicks into an extension of warm physical touch. 

---

## How it works

- User’s heartrate data is streamed from their smart watch or device to their paired Qlubi system via a local HTTP connection  
- After establishing a baseline, a maintained spike in heartrate indicating stress may be detected  
- When this occurs, the system sends a signal via MQTT to all other active devices in the system who begin to gently pulsate indicating that there is a in-network user in distress  
- Those receiving this message can then tap their Qlubi on the head three times, sending a signal back to the original device telling it to begin pulsating a different colour indicating that they are stressed and someone has reached out  
- When there are no other active users or there is no response after a certain time the Qlubi acts autonomously, entering a slightly different alert mode simply to alert the user of their stress  

Through this others can pick up on what their friends and colleagues are feeling, allowing them to step into their space and be there through the Qlubi

---

## Design Intent

- Qlubi is currently developed as a prototype device intended for experimentation, iteration, and open maker development.
- The system is intended for both end users and makers interested in building connected devices, wearable interaction systems, and emotional communication tools.
- The device is built around:
  - Lolin S2 Mini microcontroller  
  - WLED compatible LED strip  
  - Lolin 1 Button  
  - A wearable capable of monitoring heart rate  
  - A sensor logger app on a mobile device synced with the wearable
- Everything included is open licence and intended to be shared, modified, and expanded upon by the community.

---

## Hardware

- The hardware platform is centred around the Lolin S2 Mini which provides wireless connectivity, local processing, and LED control capabilities.
- The lighting system uses compact WLEDs with 7 LEDs which provide device state feedback and interaction visualisation.
- The button is the Lolin 1 Button which provides touch interaction and allows users to physically respond to incoming network signals.
- Users must 3D print their own parts using the included enclosure and component mounting models provided in the repository.

---

## Software and System Behaviour

- The board firmware and laptop side software together manage the communication and interaction logic of the system.
- Firmware functionality includes:
  - Subscribing to wearable heart rate data streams
  - Establishing and maintaining a baseline heart rate
  - Detecting deviations from baseline values
  - Managing device operational states
- Network behaviour includes:
  - Communication using MQTT messaging
  - Broadcasting distress signals between devices
  - Handling pairing messages and confirmations
  - Managing response signals between users
- Laptop software functionality includes:
  - Acting as a bridge between wearable sensor logger data and MQTT broker topics
  - Publishing heart rate data to Qlubi devices
- Interaction logic includes:
  - Button tap sequences used for mode switching
  - Pairing initiation and confirmation
  - Triggering response signals
- LED behaviour communicates:
  - Device state
  - Incoming network signals
  - Pairing status
  - Response confirmation through pulsing patterns and colour changes

---

## Open Source from code to form

Hardware: open, reproducible and customisable through simple 3D printing  
Software: open source Circuit Python  
Concept: adaptable and extendable  (GitHub) 

Whilst having a specific aim, Qlubi’s framework allows for an extremely wide array of customisation as users print parts to make their Qlubi theirs and open code allows one to stack on as many features as they can think of.

---

## Build Requirements

- All that is needed is a 3D printer.
- No soldering or glueing required as all parts are friction fits and the enclosure is designed to hold every internal component securely.
- The only adhesive required is a strip of double sided tape used to hold the LED strip to the back wall of the enclosure.

---

## Assembly

There will be a separate document that contains full assembly instructions, build order, and placement diagrams. This repository references that document for the physical build process.

---

## Setup and Configuration

This section will contain:

- Firmware installation instructions  
- Network configuration guidance  
- MQTT broker setup instructions  
- Wearable sensor logger configuration  
- Device pairing instructions  
- Troubleshooting information  

This will be completed once the full GitHub repository structure is finalised.

---

## Customisation

- Qlubi can be printed in any colours and materials the user wants.
- Decorative and functional variations can be created using the provided 3D files.
- Expansion geometry allows attachments and custom add-ons to connect cleanly with the base device.
- All enclosure files and firmware are available for users to edit, modify, and extend to suit personal or project specific needs.

---

## Network Requirements

- One needs access to a server to set up a Qlubi network.
- The server acts as the MQTT broker which manages communication between wearable devices and all connected Qlubi units.

---

## Why this matters

Qlubi incorporates this connected but anonymous form of network to both remove the shame of reaching out that drives disconnection whilst capitalizing on this alternate medium to take connection beyond where it could in the physical world. One can reach out through simply because there is someone that needs to be reached and can do so without feeling uncertain as to whether it is their place to. In a world that removes intimate connection, Qlubi highlights it and advances it 
