---
layout: post
title:  "Transmitting EMG data over BLE using BBC micro:bit"
date:   2017-01-27
excerpt: "Custom written post descriptions are the way to go... if you're not lazy."
tag:
- projects
comments: true
---
Recently I took part in a challenge organized by ARM Ltd which involved using a BBC micro:bit as the main processing board in an EMG sensor device. The device sends electrode sensor readings through BLE to an Android phone, and then data are displayed on a real time graph. This project was done in collaboration with Thomas Poulet and George Kopanas. The overall project setup is shown is the picture below:

<figure>
	<a href="https://lh3.googleusercontent.com/6SwDshrvv2NECpwLYexqUu7tE0FOtiDFheF7HyCKPEoPwlzIHNSu330y5RNossYYbutsTzhVGxaG68bEFX2XJTfsEw-o1pBlzNdcAA_8o80wrIxXhSC7OevuflnQlh6rAEeFs61cXhMz4w4LWNUg8Zdj7jHh6GaqLuTfoveQ4Sf_Jh_pguQclkbR8ifo3ODFor0Llbzs5eHly8ZzENNttZcjRGClh09Zw4X_kdrOyfoDjTa9BxkvvAXynAcY1MVjOEj0hw2MQDY5BF1CnhA1ABs7sTJlYY-O077en_a9HHmslfra0Qc872IN0qsm_SwwyJyK2S72RPreC5QIqUmHvDMfDlFeRsHaDaOFl22DfpCWyBX3_JbfyPOB5Im8Pl4PZHDdVSuKkCuLlB9a6Qbh6JKj7U7BR8ZXZe-vYNdv6IzS14EmEqNzdH759-hmkc6BBEg6TDHVtAaLmnr7y80vHSQV0hU27fxa9ipSEgVF60RBi1wzWiJLiHmMSNdxKaAzVD0AHNNZ6IY4jgr6O4NYybqojJ6CkfmBsGjwavaY-2jMklHIlxmZkzrCogBEFwxrPvmS81aWJNvUb_2HVRONvJHWQdGSE_yono2EvS0=w1200-h800-no"><img src="https://lh3.googleusercontent.com/6SwDshrvv2NECpwLYexqUu7tE0FOtiDFheF7HyCKPEoPwlzIHNSu330y5RNossYYbutsTzhVGxaG68bEFX2XJTfsEw-o1pBlzNdcAA_8o80wrIxXhSC7OevuflnQlh6rAEeFs61cXhMz4w4LWNUg8Zdj7jHh6GaqLuTfoveQ4Sf_Jh_pguQclkbR8ifo3ODFor0Llbzs5eHly8ZzENNttZcjRGClh09Zw4X_kdrOyfoDjTa9BxkvvAXynAcY1MVjOEj0hw2MQDY5BF1CnhA1ABs7sTJlYY-O077en_a9HHmslfra0Qc872IN0qsm_SwwyJyK2S72RPreC5QIqUmHvDMfDlFeRsHaDaOFl22DfpCWyBX3_JbfyPOB5Im8Pl4PZHDdVSuKkCuLlB9a6Qbh6JKj7U7BR8ZXZe-vYNdv6IzS14EmEqNzdH759-hmkc6BBEg6TDHVtAaLmnr7y80vHSQV0hU27fxa9ipSEgVF60RBi1wzWiJLiHmMSNdxKaAzVD0AHNNZ6IY4jgr6O4NYybqojJ6CkfmBsGjwavaY-2jMklHIlxmZkzrCogBEFwxrPvmS81aWJNvUb_2HVRONvJHWQdGSE_yono2EvS0=w1200-h800-no"></a>
	<figcaption><a href="http://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>

You can find more info about the EMG sensors and how they are connected to the micro:bit here.

Bluetooth low energy
BBC micro:bit comes with a Bluetooth low energy (BLE) antenna, which is designed for reduced power consumption thus making it perfect for our use as we need to continuously transmit EMG sensor data. The micro:bit is configured as a server that waits for GATT requests and sends data, and our android phone is the client that initiates the connection and receives the data from the EMG sensor.  We use Nordic’s nRF UART over BLE in order to transmit data.

Transmitting data through RX Characteristic
Connecting the phone with the micro:bit is pretty trivial on Android. There is a code sample from Google and you can find all the required information on their developer site.

First we have to scan for the avaiable devices and then select the one we want to connect to (in our case micro:bit). After the connection is initialized we enable indication by enabling ENABLE_INDICATION_VALUE flag and we wait for data sent from micro:bit. Data are sent to RX Characteristic (UUID: 6E400003-B5A3-F393-E0A9-E50E24DCCA9E) and then data are plotted to the phone screen using Graphview.

Here are some pictures and a video of how things look when everything is connected:

<iframe width="560" height="315" src="//https://www.youtube.com/watch?v=8L-78S_hh5o" frameborder="0"> </iframe>

