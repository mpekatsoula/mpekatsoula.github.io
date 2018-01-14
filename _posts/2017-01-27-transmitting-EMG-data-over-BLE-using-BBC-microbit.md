---
layout: post
title:  "Transmitting EMG data over BLE using BBC micro:bit"
date:   2017-01-27
excerpt: "Using a micro::bit for transmitting and an Android smartphone for displaying EMG data"
tag:
- projects
comments: true
---
Recently I took part in a challenge organized by <a href="https://www.arm.com/">ARM Ltd</a> which involved using a <a href="http://microbit.org/">BBC micro:bit</a> as the main processing board in an <a href="https://en.wikipedia.org/wiki/Electromyography">EMG sensor device.</a> The device sends electrode sensor readings through BLE to an Android phone, and then data are displayed on a real time graph. This project was done in collaboration with <a href="http://blog.thomaspoulet.fr/">Thomas Poulet</a> and George Kopanas. The overall project setup is shown is the picture below:

<figure>
	<img src="https://lh3.googleusercontent.com/VC5Xp803F_uQGAtTv6TGyUojgJHWw8Nu6IkHPhBNI0gCGEuKeNv7vVjH8c7Yv7CmfHBYcpE6ZiZiSPktyAo5VE3HwmtS2udW0fEHUSZhkU96J5jX2ktP-nW4unqi_VqECORqxifRS4nruXp8SvQ8u8-7NzIBZ0c5L0aQdk3R7_bHupy8ZXhm0JWSNtit8Dk3KRNOYTxELNr91_A4T8cONR2lsCQbRsOJbdF_YoHama9TtSMZ7i-Aepu0cQ7H-METUnU3WzEn1LMpusRfQqm5C-bI6YxkkSxemBhLNlawLkDI4iBG9_7kFAcfN5UAv4xLI6Jr4WdCrD_VSDrDJ0tox_tp78ulIs4GUwHme7C55ynOtfoKTLAC5aOCMlus2mDIpJhR7wIBxLc-auTtRtumORbW7wUHzsC2_YeAqfiTx45lcKFw2E4wK82othMbkTkxu2vUDuWK2P4XAAPt9s5oqtAuTdhSf_DKKFgmr2Vg8A-dBOJkdte6gX1J3xEsmHikVnwdsM4t6tPUqouLODB9oJ-AI5w-M5phdyLUl5sg_Wm_zNupOq5TioMC6jW-PeckF84iveT0YpPZvdKjNf0UFi8m7pvWyzGuSyP6-p44guTA2fq3bxhV7HFEPRr88OekqkKDjbNEq1v9mQVQb7vqj3_bvi7VBCob=w746-h382-no">
	<figcaption>Design schematic</figcaption>
</figure>

You can find more info about the EMG sensors and how they are connected to the micro:bit <a href="http://blog.thomaspoulet.fr/portable-emg-microbit/">here</a>.

### Bluetooth low energy
BBC micro:bit comes with a Bluetooth low energy (BLE) antenna, which is designed for reduced power consumption thus making it perfect for our use as we need to continuously transmit EMG sensor data. The micro:bit is configured as a server that waits for GATT requests and sends data, and our android phone is the client that initiates the connection and receives the data from the EMG sensor.  We use <a href="https://developer.nordicsemi.com/nRF5_SDK/nRF51_SDK_v8.x.x/doc/8.0.0/s110/html/a00072.html">Nordic’s nRF UART</a> over BLE in order to transmit data.

### Transmitting data through RX Characteristic
Connecting the phone with the micro:bit is pretty trivial on Android. There is a <a href="https://github.com/googlesamples/android-BluetoothLeGatt">code</a> sample from Google and you can find all the required information on their <a href="https://developer.android.com/guide/topics/connectivity/bluetooth-le.html">developer site</a>.

First we have to scan for the avaliable devices and then select the one we want to connect to (in our case micro:bit). After the connection is initialized we enable indication by enabling <a href="https://developer.android.com/reference/android/bluetooth/BluetoothGattDescriptor.html#ENABLE_INDICATION_VALUE">ENABLE_INDICATION_VALUE</a> flag and we wait for data sent from micro:bit. Data are sent to RX Characteristic (UUID: 6E400003-B5A3-F393-E0A9-E50E24DCCA9E) and then data are plotted to the phone screen using <a href="http://www.android-graphview.org/">Graphview</a>.

Here are some pictures and a video of how things look when everything is connected:

<figure class="third">
	<img src="https://lh3.googleusercontent.com/-_3iElJ8gPQkA9RuNWUtZEfsYGydhyckgr3M06SYQcEd5KqFedKsrzseUjuN74CbjC7Wg1CnyScudccGZb0kg2e5OYwvvFauP6Kerrdg6JiXhr_zfxixNDKe_T9uLzuBou6r_JnWsXwpA8CXtgcZILlvtvtDx37WVZugxHixo8TCT3hzLCOlhQIRgQmIvMYwSr8H9th-cpy7wwWHfAervycmn7-RPTS0ATjQAaOe4SJITVjd8BdU-XxYvf3Sl4xpJsCLKQNM_votrjq0J6dZZgwCR8u7KdtpXF9bUjLNHM3xsEgVbDAjclqqBjlG2oqZBp9XfKpLHCJqFDfPw5NZNq01oEjPaScngZAU9YwVSq--XFF93AzcQP1OrIb3N0BBe0SKYakruifQLZAAh9-j8o23X_nucSuKwdYUXkBSwWqO08ut8XG6YXR6wQ8P7evvPv3V56ePTkQgKIY_tIdvHAke6Qcw9Rt42Zjp-DwRFoD_U93TaNuTak-gTI433mIFP5VtVjHLLTXJWKcEiLGteYBgm3myaACr0JH3bpjOcqRv_wsb6gRfWmv2nYuG_BjPAmasoC1eaqqyf1CI2L1N6yi_u8pfqIN5yhGRbEcl9bSlnK6BOMZDGrw39sIuRmylf50PWtZHV03JgjTvByEBwueSJ6i8l_gh=w1200-h800-no">
	<img src="https://lh3.googleusercontent.com/b6eZHfyWY0mv0L7HfjuHaCV4nrhA6BhYv2onVoHURHmK7TQt7XW91lUQlaZsnvpTg7PKqNyNEi6CSfzyvSK1qpsqyEsw4nkH7fb--vK8JFcjQ90T0lUVocyoT9x6AnVOPhjNnwA6CgmoFREnlc3Yj9MRidl48LtjMSw8vgp25O5TokS97w6kvEjsLVQaVQD3vsoyfxS-jgrpJ72z8IIZ5dsKUzFOMmx1G4MBHdpwaofHC4QAmHT5DeCNzsvorPk-pKHGi1HovK9SSw7Z81e9CB7TYRTcDE7V0lTefVXDs-HHyONjiCVE52hK9RljJ3qUZyJtylqHRw3Jc-pFts0kMIu5rnGmwj0C87QVloFHcGHF3OG414qQQ6StgdoWI_hQHOHKzYoC2S_onDGXS3VMqD0DQ-H-6bw9YJsbjaLDOSoKwUA97iKRUYwr8R6siQcGxjVJ1LA-GL020OQKsubbMjO1qzAcfc0fS4-zkm5Otj6YvDwtkJK4-DcvpmhXEsU231QtN90ZgnDZ4FNizEtflTl1OcWqlJN7xeewtHtdfAKndbl68byB-UqYgXG-0IQ0J_A5E_q-YTMWtlrI1r9JpgItrob50nC1U9qfCA63rtFYDjHQIODxfQ7LP-kLNaTkPPZoVRDS5bir2aC4eiGSl49Hr6Io01tP=w1200-h800-no">
	<img src="https://lh3.googleusercontent.com/Ym4ZWcLo6-XxWC4u6kDkEK2yeYTHwVcsRRd9Lx7f-czgNpt37J7oa8r4YRGnp-I0bN6pAOPlpxRdYCC7Slyuantqicavzir1KYBRWnB24Gea0rdlRQn9aC12JkYOlrqtEjOMe_JmEF3aLZnkkqTeK3ESHnBqYlylNSi9dEZCDC47-OAEskoaDxsjERykV63Nk7mhz-9mTxAKYFaqPs7lvoovT0_fXmrHpmlsU5l2ugNpBPYQ7jRKcZlegwHsX0F1l7_89LTW9iwC1nhH7REyypl4SKFADLXiS5qw-0AeJT4QYwtb0af2ahbLVdLMrW5YsjcatkWxvfC0w0tKw1NkVb-RZYVcBsBNl8LM0PvbWx_I8pVfxzpwM0zPPbbyVusEB4nlKNh2GTFOmWXF0eYRkXHlhSiMqCJNJQkHrO_ZlspTkc3VnyCdYrXnDU7Y8c8Zu8TRRD8jJqYsYbO2KCUFQKi06coAi-IVN9JpmeXnLFYnDmHIUY6RCGwkdEabdFg-DzSh-ra3fkCNGNfk_goZU9RBG28F0ZHr78E0obDhf32NioXHWl0JlH6J7f9A7hBUfiW_-QakqZR8NZAjHpmockMwP6diHGSL4__6SLq2LhFhTu-ejbGuw_7wuGAzTxsmcelRjIMB47j5lu1HVAChIg4VFSvJ8MTa=w1200-h800-no">
	<figcaption>Prototype of our design.</figcaption>
</figure>

<iframe width="560" height="315" src="https://www.youtube.com/embed/8L-78S_hh5o" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
