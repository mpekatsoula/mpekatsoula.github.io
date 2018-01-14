---
layout: post
title:  "Two player pong game using accelerometers"
date:   2013-06-21
excerpt: "Embedded systems project using Verilog, a Spartan 6 FPGA, and two 3-axis accelerometers."
feature: https://lh3.googleusercontent.com/CC8MTWA8kml8BtBvKk5_bwD7TDC39G3Vn5KYv4O6i_FjF1FCz2Sqq32FYn9M4l6H05X90D4i1Wvt_TylTBJFDiD2F5P1KT1SwWXwwJcRHhX4YxV1gvanHFaMzJlZqfDsc_8Ic2UMW1NxFRb1y_l25QZIdFjjB5T4nqhoLf-aT_hLFbMKxzz863NUEiheGOBm5vOB3MFrBD2IHN6d-BbpeVDL1n6GIbYiO1TtoFDdPi93R8l3DhZ2AmXGI_iErpYoX3L3i8eyLyv1-7KpOmWa068tRKanQY6lTWnIhIPGkQzRw3eVjVqyAbB_gc2COg8GEHgULiua3chdlvIp5846Y-trEyt7KMeeATTUcrjrlw_drXGtTAp1fp0-sE3ItOXYKfJONkWE9qC2v1LxKjRJFC8k5gC-rg36CXE8a1rARAs-VDm7IkW6UmN5QzhBhPwP8JTukAJGwjhNjVqs5XrUR8qIIWETmvSavMING5_xLp4ekb1E3_KHO7eQSyAG3cjuuQwzvIC92aTUn54xo4-8GAdkYiiPdg9HRMk2m7-BCjfa9R4syA2aelXnbpj1GR-IA6vjrvZoy10NHX1azzG0pQMaGy9ApgyQWxPxFdiCBPwOTeW3Apaz5lI1dNsTlcknFBV5p3DGELI94OvIePskcuBQtlCH4i2m=w1308-h804-no
project: true
tag:
- accelerometer
- FPGA
- gaming
- Verilog
- VGA
comments: true
---
<figure>
	<a href="https://lh3.googleusercontent.com/Gh3u_podMJ22w7Ow80kgF1TcQ2XJH6czPWgXjHkr7Glwuoi9N4Aua7Uf_vLu3Shw98xHdPS7Dck2YVeqinYii31QCuqBffHbC6WLKE0srdoOr1RaRU0k5DLerRNzJSYSF1kI-GXufCKLGYJsh9Pyy9JWstedRo9ElwZEAfLuyX5Pns2t2pGKRLkfVX15NNymz5XrQJqA_Iintx9tBFrkLZga5tlqiDnnKdQw-slbEKVkd0AQSfR02x-yQAmSaqs9nwdmkCMGfRDYRY1KvJUjut7ZyxCxNW3HpbxM3I1Zpnx3krfViVbM8LqB9V-Fehdn72Pb4hLpxVppRuQCb34Jr00NPkEVQwKqy7o3GCRFEHzYdmPFjqpY-pSSGTD7cP_PuCqS4T5jVMgPruaBnxOt9O_uZKYdvcOl05BMM1DPlyZiC2bILsOohvwWhXBHtiN1NPgWif0kRFrz6hnJCpSSjmKVLPlUj-J8-LZy60IXiffTvZw2ijT9iAdd9UMf9E_3fsEBf4iEqCTsYbVOV09J4ugIg5JkSaYnEDWGAoLlcgsIInfe1Go0UACy_pZ3LNfW7UUWPgzHwTD4ohKJ-9cLWYl5LoPnaN3MZmKF6iCNyJdwa9HeF3C5837KdtOpnQQEvCxFzfdco1pdPgkn0dvSMGHUHya-azf0=w683-h910-no"><img src="https://lh3.googleusercontent.com/Gh3u_podMJ22w7Ow80kgF1TcQ2XJH6czPWgXjHkr7Glwuoi9N4Aua7Uf_vLu3Shw98xHdPS7Dck2YVeqinYii31QCuqBffHbC6WLKE0srdoOr1RaRU0k5DLerRNzJSYSF1kI-GXufCKLGYJsh9Pyy9JWstedRo9ElwZEAfLuyX5Pns2t2pGKRLkfVX15NNymz5XrQJqA_Iintx9tBFrkLZga5tlqiDnnKdQw-slbEKVkd0AQSfR02x-yQAmSaqs9nwdmkCMGfRDYRY1KvJUjut7ZyxCxNW3HpbxM3I1Zpnx3krfViVbM8LqB9V-Fehdn72Pb4hLpxVppRuQCb34Jr00NPkEVQwKqy7o3GCRFEHzYdmPFjqpY-pSSGTD7cP_PuCqS4T5jVMgPruaBnxOt9O_uZKYdvcOl05BMM1DPlyZiC2bILsOohvwWhXBHtiN1NPgWif0kRFrz6hnJCpSSjmKVLPlUj-J8-LZy60IXiffTvZw2ijT9iAdd9UMf9E_3fsEBf4iEqCTsYbVOV09J4ugIg5JkSaYnEDWGAoLlcgsIInfe1Go0UACy_pZ3LNfW7UUWPgzHwTD4ohKJ-9cLWYl5LoPnaN3MZmKF6iCNyJdwa9HeF3C5837KdtOpnQQEvCxFzfdco1pdPgkn0dvSMGHUHya-azf0=w683-h910-no"></a>
	<figcaption><center>Final working demo</center></figcaption>
</figure>

This two person project was completed through the course of Embedded Systems at the University of Thessaly, Department of Computer Engineering. In the context of this project we implemented the classic pong game using a Spartan 6 FPGA, and two 3-axis accelerometers. The code is in Verilog and you can find it on github ( link at the bottom of the page ). The project consists two parts. First, the connection with the monitor through the VGA and game logic and the connection of the accelerometers through the SPI interface.

### VGA Technology and Implementation

The first part of the project was to connect the FPGA with a monitor using the VGA output. VGA is a video standard mainly used for computer monitors introduced by IBM in 1987.

VGA video is a stream of frames. Each frame is made of horizontal and vertical series of pixels which are transmitted from top to bottom and from left to right, like a beam is traveling through the screen (CRT displays actually used a moving electron beam, but LCD displays have evolved to use the same signal timings as CRT displays). Information is only displayed when the beam is moving forward and not during the time the beam is reset back to the left or top edge of the display.

First we made a VGA controller module that generates the correct signals. The signals that we need to pass to the VGA DAC (Digital to Analog Converter) are:

<figure>
	<img src="https://lh3.googleusercontent.com/jhBqIzm46CTuLvdqWamWPHQDQ3uq2XDAHIdqgHlv69gN4CbPOqUkqBVo6UFfBkIk63lKFcG5gjvpki8eYjwTqP7dw8ysczHf8dWy3mr4WSTSQ0hQJ9hQN0gZqMXVmdAgvA6_ICQ7luh877JjnbMIRE2prbKQxQvAxPU4YrLshShQJL48E1YmWpfud5pgIXm5YRoY2kI-j62b_PLlgkh5-GkdjzJk6K9mvrgBqEMFxcvYhNJphmMAYC8kEzfheD4IEHCHoKmbKouyjvS6AbdHMfPi84dDRjq7-LQBlG-RZWqqUUF8Wmdh2Pzfdz81-Kj9dC3zCvCNK1JdEz1W2faK-R1SvWIpW_yzx-25KZWAxWovQscEINl_Kp2xinvdw3kNS0IFdXNePwhRFQZCn482OFnV_rLgXTkleDvtBF2gt7IovhoJrJgdUOXjChmAU_XnEw5E3rf5HwFBp4Gz4jIW-dga5rfVNNZNRCG_kboqh_cVQOnivXpwccR4O_zVgE0CeZXc5NLx_gVWqaR_iqLGj0IFf-7tqQ88LI7ebcI5AcUcGKSbUUrum7WM3jXSsWJuUrHgglE39u7aawvzD0Ky-TzFN_3vkTbsPjvTKT18x7EtsTtelw-2ImgnmfvTgvphD9rroOmLXC3FlysUKuvXsEPOllaMbXMW=w293-h299-no">
	<figcaption><center>Digital to Analog Converter signals</center></figcaption>
</figure>

* Pixel clock
* Vertical Sync
* Horizontal Sync
* 3-bit Red
* 3-bit Green
* 2-bit Blue

Pixel clock defines the time available to display one pixel of information. With different timing values we can achieve several resolutions, such as 800×600 etc. Vertical sync defines the refresh rate of the display and horizontal sync is used to indicate the end of a horizontal line. We use two counters, hcount and vcount that count the pixels in the horizontal and vertical lines. We can determine the location of a pixel in the screen (x,y) by combining these two counters.

<figure>
	<img src="https://lh3.googleusercontent.com/JDJG1m1NQPdg_ivQqFDui3wITim4D7qvRIZOTDn5Iv4erkCOHyOBGabCP2OmHAuUxBxK3fPvlZvOFjA2Pu90xEYV0VdFQn87OSJpkptT7wkZtnYaT3xMhEbrNtvzdM2FCpK_Ho56-EUk5sM2kQl4tp20hjg0frEAxSBSxvF6-3n85nioMnP86_1uExspDGDdULZWXttduT-sthoxOeGMz9NBGiJttcA_ABnHeTQyRxoGsHewUDVn94jDllhpk8IZ3-sT7cao99HVl3N9IQHvzq17_grjrI2bie9C6M44NO8_ic0mUjMS1vEes9NPrigK_x9IGFzRgdAExuhemeVheBgBp3U0DFxHKj2GTHO0ySrl77m8hqyKHMPmTX9hPAap9PMe5p0mV9EHXORsWpcdiIkprRim4pWdf6z3BiV-EpaE_FXfguQxUizQrMMGTPDhHy3LocHUWd8I2J_GIbxOETLu-UkT7UqjNHjHWQhqOq9sMHPTsgYr9MLnMRQpnccNJC5NTy1KqpCFDuSDo3VMdRmLRJ68eDEFtwDq97YUhKq1XwZEc1k9BMTK-ttYvKxu09R1YOXrw2-RcEhZ9J_qsLIybj8clw9KUvolPaZ5cF-Mis4tyMYqS_vM_ukMzG8AKjTjcwOtY5sRiyo1vDzAAyoHzZeJwIZF=w583-h594-no">
</figure>

Each line of the video begins with an active video region, in which RGB values are output for each pixel in the line. Then a blanking region follows in which a horizontal sync pulse is transmitted in the middle of the blanking interval. The interval before the sync pulse is known as front porch and after the sync pulse back porch.

There are many VGA timing values that can be used, in order to support several resolutions, as we can see in the table below:

<figure>
	<a href="https://lh3.googleusercontent.com/oO2p4P6JTg2OE4Cae5Nx30fJ0jtirLz0h3vRgb3C-iQjoywkBNZgfdPzc5MRIDDG3S-SNKaPMuvEletJ5BtUWgtM5npdFharERHYACTf2cfWSX4__-mJqIiM7GbnZ6Yh6vvXPFW-UeXrZCqoWu7DhAedC_ZP4-w_VcHLhd_xVQtAFFROsQMj29im3CdATjZP9mApRMxcX28A_5c3oplVWij9YWAt8fEmPbyoGQEHzBubn_Wqe6GS3imEvbw3nZvCLSCeNzTr6g8Fj9Hi576KJQ28kq5j--hOYQVYEsvJ3-yyL5q4LAG_NT6NZNGkPjVvz5XPn0zmvsb_1ZHb3nFwn_SH_Fyk5JFE244PXia1DmQTd6JyBlSEfhKm_o8IWFzMa4O3m60gsl40tqRYjZzuZVc577sRj-ExqTtiGO3CEalH3xrOYw3h5ZyrmWG5CQph_2kYL_lgWujaOTh8wkas9FWI8oIRd0gZmmH-0voNc2lpNdwO_PmhGxbdjOozwtk4kyfHOWmSbiVir6KaRBsZOAuCS1B2HeBGXocflDRzHcolOyXlb0-Lkjub9UZy0gbe9nM9Q3jPFY46V6N3oCrUPH5J_O4iXGGd61yoKHR-l3hZ0alanR0I3Ddhi-325rxNJv3hxqdTE1-OBYyFYuos18ljnyKZxyIM=w572-h475-no"><img src="https://lh3.googleusercontent.com/oO2p4P6JTg2OE4Cae5Nx30fJ0jtirLz0h3vRgb3C-iQjoywkBNZgfdPzc5MRIDDG3S-SNKaPMuvEletJ5BtUWgtM5npdFharERHYACTf2cfWSX4__-mJqIiM7GbnZ6Yh6vvXPFW-UeXrZCqoWu7DhAedC_ZP4-w_VcHLhd_xVQtAFFROsQMj29im3CdATjZP9mApRMxcX28A_5c3oplVWij9YWAt8fEmPbyoGQEHzBubn_Wqe6GS3imEvbw3nZvCLSCeNzTr6g8Fj9Hi576KJQ28kq5j--hOYQVYEsvJ3-yyL5q4LAG_NT6NZNGkPjVvz5XPn0zmvsb_1ZHb3nFwn_SH_Fyk5JFE244PXia1DmQTd6JyBlSEfhKm_o8IWFzMa4O3m60gsl40tqRYjZzuZVc577sRj-ExqTtiGO3CEalH3xrOYw3h5ZyrmWG5CQph_2kYL_lgWujaOTh8wkas9FWI8oIRd0gZmmH-0voNc2lpNdwO_PmhGxbdjOozwtk4kyfHOWmSbiVir6KaRBsZOAuCS1B2HeBGXocflDRzHcolOyXlb0-Lkjub9UZy0gbe9nM9Q3jPFY46V6N3oCrUPH5J_O4iXGGd61yoKHR-l3hZ0alanR0I3Ddhi-325rxNJv3hxqdTE1-OBYyFYuos18ljnyKZxyIM=w572-h475-no"></a>
</figure>

For our project we had a resolution of 800×600@72Hz, so we created a 50 MHz clock, from the 100 MHz clock input of the Spartan 6 and the horizontal and the vertical count have a total value of 1039 and 665 respectively. Based on these numbers we calculate the exact time that the hsync and vsync are set active high (both signals on this resolution must be active high) and we connect them to the FPGA pins.

### Pong Game

Based on the VGA module we draw on the screen basic shapes such as the paddles and a square dot that represents the ball. The paddle drawing is done at the draw_shape module that given the (x,y) position of the top left pixel, creates a 128×16 pixels rectangle. The same happens with the ball that is 32×32 pixels. Also we have a module that creates the game board; four lines for the perimeter of the screen and one vertical line at the half of the board. Each of these modules, output the pixel locations of each shape.
Ball_movement module takes as input the location of the paddles and the ball and does the necessary calculations for the ball movement. Ball moves at a constant speed of one pixel in x axis and one pixel in y axis. If ball hits the up or down board limit or one of the paddles the trajectory is changed. Also in this module we check if the ball hits the right or left limit, and if yes, a signal is generated to indicate that a player has won a point. Whenever a player wins the score is updated and displayed on the screen. If a player’s score reaches 10 points then the game is over and a message indicating which player has lost is shown. Then the game resets to its initial state. Finally this module outputs the pixel locations of the ball and the paddles and they are driven to the output_pixels module that generates the final output that the monitor will display.

A snippet of the code that checks if the ball has hit the paddle:

{% highlight c %}
// Find collision between ball and the paddles
if ( ((ball_y <= paddle1 + 128) && ( (ball_y >= paddle1 - 32) || ( paddle1 <= 32 && ball_y <= 128 ) )) && ball_x == 18 )
sw_x <= 1;
 
if ( ((ball_y <= paddle2 + 128) && ((ball_y >= paddle2 - 32) || ( paddle2 <= 32 && ball_y <= 128 ) )) && ball_x == 750 )
sw_x <= 0;
{% endhighlight %}

The numbers showing the score are in seven segment display format output and are generated in the draw_score module. Also we implemented a pause game function by activating the switch T5.
Since Nexys 3 board has a reset button that only erases completely any program loaded, we use switch V8 as a reset signal for our project.

3-Axis accelerometers

An accelerometer is an electromechanical device that will measure acceleration forces. These forces may be static, like the constant force of gravity, or they could be dynamic caused by moving the accelerometer. There are different types of accelerometers depending on how they work. Some accelerometers use the piezoelectric effect; they contain microscopic crystal structures that get stressed by accelerative forces, which cause a voltage to be generated. Others implement capacitive sensing, that output a voltage dependent on the distance between two planar surfaces.

In our implementation we used a 3-axis (one axis for each direction) digital accelerometer powered by the analog device ADXL345 and took advantage of the force of gravity on y axis, making the paddles move by tilting the accelerometer right or left. We connected the accelerometers through the SPI interfaces. SPI operates in full duplex mode and uses four signals: Slave select (SS), serial clock (SCLK), serial data out (SDO), to the accelerometer and serial data in (SDI), from the accelerometer. Devices communicate in master/slave mode where master initiates the data frame. Our setup contains two shift registers, one in the master and one in the slave and they are connected as a ring. Data is shifted out with the most significant bit first, while shifting a new least significant bit into the same register.

<figure>
	<img src="https://lh3.googleusercontent.com/px7u46RIAM01DaTzwFhHaMBrBCWG7Rs58C3Yb89xCBjYWfQntcY5jq2oaBH93a7wpid9-tx4rKNub6Ga89JCxFFu6G-3sdMnVhl7AH9puIRwoprzp996CxBWd0ptWhs0d0HdLtv4NjIPaCuZPq4tf2eaMuj3ZZ3h7_-HQH9njeDJLZ6brm_T8DlVj79Rwu8iW7pHf-K4-KDInbdO_F8n2yBFY8hxldRFOdVKHH_YJ9EjKRhLfdrLRY9ysYeIgcX7M_Ubjw48QyltOytfOJL4F0cczX_SFHelpG5hiw2RISD6xxKWCqQpHQ6Mc-3dYOHycgTo2SmyqOZQXGEkScQ-fn4bRdlS4T7E8AQveee0OmxQG48fiXvVdr8OtbynmqtV7JrGRgg-9DUvPBmwC3Hgz5acwVgHDfw6hJmptDJSml9JqbdQqaT9y2ch-TCblOgSG3vCic-jLDbSAcQsTqjmLODO5SvUGT8GMv9JlpM4xdyE_Hv6YiB6K12AoN1e1qnbe8Dj_qhG-9q7c9nUF9aSFA2KWid-A77FzVIyFL8MFFOZEu3tW86Tk6KJCIcwFzVsGKW8VaYSOH7LqulTDKQGeq6yyG0bDsTL-OeNJulbjXnzOuEcbFLWohA-n-1ZlOWklkx2hzSR2it3v4TYRYIE3f7y-v5S91Uk=w500-h156-no">
</figure>

We initialize the transfer with a 5Hz clock and we transmit/receive data at 22.4 kHz rate. The accelerometer is configured for +/- 2g operation. To convert the output to g we have to find the difference between the measured output and the zero-g offset and divide it by the accelerometer’s sensitivity (expressed in counts/g or LSB/g). For our accelerometer in 2g sensitivity with 10-bit digital outputs, the sensitivity is 163 counts/g or LSB/g. The acceleration would be equal to: 𝑎=(Aout−zerog)163 g. We didn’t have to make those calculations for the paddle movement. We just take the accelerometer output and we move the paddles accordingly based on the table below:

<figure>
<a href="https://lh3.googleusercontent.com/ItwJu7sWcxrR2iGsxKgBEXCwRB1E5p9XZhuXGb3jEgKsev199iuTWvduEg0boYtRKGgk3FWbE60Pn5g1AAbISjuWuYJGjmyRCdg-Fl4mgrB_cbbfYnmG8_ssIFN_Kj2ym7Hq36qenr8kMFyzPNzSjAVLV7GZsKAf8sz5NvqpgxaSfh2FAaxqiODbHk7Sieqh0zjaIfhJzeM1PG4STYF_aS0FJCXZgF7DK3XDRCmnV9iiO1hRTcRTdoOgkKFzNEi_KpGshHjb_g28148BWFP95tlWtChmwdaD4MKx3-lxwLqPEYB6WZzr-ZbXWaQZVNMC7nmcDwE4lUDp2tLszAXFpGqfVfG9tMoVHEMvM9GKXfQjQLjPCWKZ15LbSofd1_gPX714Zi2Fr8J0b6uILY4q9i97H5WHVS97eVfY8hNRgy1T2RxpMM6Bm4NsPIPmMlc9XskN4gYV-LVys4TWiPb_AmnhMknIxK_XDHismxGLk9N6dO2a7RvLpPmjb0ImQXxSmnzn9SPhGmtcXfmtYI8llym875lJuRxR3T5E5BmwAzoAdlCrIrZjkoedP5m5lbJh6ZWyox1eSmXdkEQ5FJuHU52z7l20r3gVdtBBrHl1PGMSzP5mgBITwHwMv3PBSywDXHgCgf6Gkd03oTWlQFv-jlpg7SxU_WRM=w1100-h468-no"><img src="https://lh3.googleusercontent.com/ItwJu7sWcxrR2iGsxKgBEXCwRB1E5p9XZhuXGb3jEgKsev199iuTWvduEg0boYtRKGgk3FWbE60Pn5g1AAbISjuWuYJGjmyRCdg-Fl4mgrB_cbbfYnmG8_ssIFN_Kj2ym7Hq36qenr8kMFyzPNzSjAVLV7GZsKAf8sz5NvqpgxaSfh2FAaxqiODbHk7Sieqh0zjaIfhJzeM1PG4STYF_aS0FJCXZgF7DK3XDRCmnV9iiO1hRTcRTdoOgkKFzNEi_KpGshHjb_g28148BWFP95tlWtChmwdaD4MKx3-lxwLqPEYB6WZzr-ZbXWaQZVNMC7nmcDwE4lUDp2tLszAXFpGqfVfG9tMoVHEMvM9GKXfQjQLjPCWKZ15LbSofd1_gPX714Zi2Fr8J0b6uILY4q9i97H5WHVS97eVfY8hNRgy1T2RxpMM6Bm4NsPIPmMlc9XskN4gYV-LVys4TWiPb_AmnhMknIxK_XDHismxGLk9N6dO2a7RvLpPmjb0ImQXxSmnzn9SPhGmtcXfmtYI8llym875lJuRxR3T5E5BmwAzoAdlCrIrZjkoedP5m5lbJh6ZWyox1eSmXdkEQ5FJuHU52z7l20r3gVdtBBrHl1PGMSzP5mgBITwHwMv3PBSywDXHgCgf6Gkd03oTWlQFv-jlpg7SxU_WRM=w1100-h468-no"></a>
</figure>
	
<figure class="half">
	<a href="https://lh3.googleusercontent.com/CC8MTWA8kml8BtBvKk5_bwD7TDC39G3Vn5KYv4O6i_FjF1FCz2Sqq32FYn9M4l6H05X90D4i1Wvt_TylTBJFDiD2F5P1KT1SwWXwwJcRHhX4YxV1gvanHFaMzJlZqfDsc_8Ic2UMW1NxFRb1y_l25QZIdFjjB5T4nqhoLf-aT_hLFbMKxzz863NUEiheGOBm5vOB3MFrBD2IHN6d-BbpeVDL1n6GIbYiO1TtoFDdPi93R8l3DhZ2AmXGI_iErpYoX3L3i8eyLyv1-7KpOmWa068tRKanQY6lTWnIhIPGkQzRw3eVjVqyAbB_gc2COg8GEHgULiua3chdlvIp5846Y-trEyt7KMeeATTUcrjrlw_drXGtTAp1fp0-sE3ItOXYKfJONkWE9qC2v1LxKjRJFC8k5gC-rg36CXE8a1rARAs-VDm7IkW6UmN5QzhBhPwP8JTukAJGwjhNjVqs5XrUR8qIIWETmvSavMING5_xLp4ekb1E3_KHO7eQSyAG3cjuuQwzvIC92aTUn54xo4-8GAdkYiiPdg9HRMk2m7-BCjfa9R4syA2aelXnbpj1GR-IA6vjrvZoy10NHX1azzG0pQMaGy9ApgyQWxPxFdiCBPwOTeW3Apaz5lI1dNsTlcknFBV5p3DGELI94OvIePskcuBQtlCH4i2m=w1308-h804-no"><img src="https://lh3.googleusercontent.com/CC8MTWA8kml8BtBvKk5_bwD7TDC39G3Vn5KYv4O6i_FjF1FCz2Sqq32FYn9M4l6H05X90D4i1Wvt_TylTBJFDiD2F5P1KT1SwWXwwJcRHhX4YxV1gvanHFaMzJlZqfDsc_8Ic2UMW1NxFRb1y_l25QZIdFjjB5T4nqhoLf-aT_hLFbMKxzz863NUEiheGOBm5vOB3MFrBD2IHN6d-BbpeVDL1n6GIbYiO1TtoFDdPi93R8l3DhZ2AmXGI_iErpYoX3L3i8eyLyv1-7KpOmWa068tRKanQY6lTWnIhIPGkQzRw3eVjVqyAbB_gc2COg8GEHgULiua3chdlvIp5846Y-trEyt7KMeeATTUcrjrlw_drXGtTAp1fp0-sE3ItOXYKfJONkWE9qC2v1LxKjRJFC8k5gC-rg36CXE8a1rARAs-VDm7IkW6UmN5QzhBhPwP8JTukAJGwjhNjVqs5XrUR8qIIWETmvSavMING5_xLp4ekb1E3_KHO7eQSyAG3cjuuQwzvIC92aTUn54xo4-8GAdkYiiPdg9HRMk2m7-BCjfa9R4syA2aelXnbpj1GR-IA6vjrvZoy10NHX1azzG0pQMaGy9ApgyQWxPxFdiCBPwOTeW3Apaz5lI1dNsTlcknFBV5p3DGELI94OvIePskcuBQtlCH4i2m=w1308-h804-no"></a>
	<a href="https://lh3.googleusercontent.com/Fhz_XDexgBsOsd_qMuckHH9imJaZrAv547MF7e51BnXmja7TQdajAsHY_4NaXhmzKeRFhunKqS9oGdYXlVEuxJB6KbPAl3ADCtccgVU0wD3_-009UYPpL9Eza8d-qe8XJ4xDlBpLOaJAIu6qF8Dfa7HKRzkq2ILAueFxKra2CHvzqw9LBwWT_daDk0-ZkYo5gijrFK4QB0Jbvo8iZ-eQfyDBuIW_AddJPoTVV3KlcaIACeknwKTMyPhIm_g4iEZt2znMWUidE-9rSMTrvO0oGWSPqYLX7Y4bnJIS0Pb3SocjLqDbZLKlFJd3lMUUBWmMw9FkQrlLcLGGumIRsR2TaDDdDBKQzHfjtbDpS_vUh0IByRGRSDJ5Fw77Uw-Ebw9iBUeiaebiIqN-DVcrAOEopPPJPyO1Itdbc1E66xWwysXKuMdl6TfnkbI6qJMpm12hzT2QeSjt7VlzkbqdAy7K-g9nR-m6Wb0QrLY-KtfgNSnjVrHFPglt7jOPR-bUhwArHYMX-gJ_0cFR2q9SbPmo2jDBDR8b6BkiyJ_lbGqFJguycrtvuFO8X5_Pg-KEduV1HFW1jE0QgvpdUIyMrGIXLJSaIMBXZvhFPgRfvGa7bQt608iU5p8pJdRluj7JPqzrbAYl9WJ6gOomIAwdHaRESKe-xQRH0hsK=w647-h910-no"><img src="https://lh3.googleusercontent.com/Fhz_XDexgBsOsd_qMuckHH9imJaZrAv547MF7e51BnXmja7TQdajAsHY_4NaXhmzKeRFhunKqS9oGdYXlVEuxJB6KbPAl3ADCtccgVU0wD3_-009UYPpL9Eza8d-qe8XJ4xDlBpLOaJAIu6qF8Dfa7HKRzkq2ILAueFxKra2CHvzqw9LBwWT_daDk0-ZkYo5gijrFK4QB0Jbvo8iZ-eQfyDBuIW_AddJPoTVV3KlcaIACeknwKTMyPhIm_g4iEZt2znMWUidE-9rSMTrvO0oGWSPqYLX7Y4bnJIS0Pb3SocjLqDbZLKlFJd3lMUUBWmMw9FkQrlLcLGGumIRsR2TaDDdDBKQzHfjtbDpS_vUh0IByRGRSDJ5Fw77Uw-Ebw9iBUeiaebiIqN-DVcrAOEopPPJPyO1Itdbc1E66xWwysXKuMdl6TfnkbI6qJMpm12hzT2QeSjt7VlzkbqdAy7K-g9nR-m6Wb0QrLY-KtfgNSnjVrHFPglt7jOPR-bUhwArHYMX-gJ_0cFR2q9SbPmo2jDBDR8b6BkiyJ_lbGqFJguycrtvuFO8X5_Pg-KEduV1HFW1jE0QgvpdUIyMrGIXLJSaIMBXZvhFPgRfvGa7bQt608iU5p8pJdRluj7JPqzrbAYl9WJ6gOomIAwdHaRESKe-xQRH0hsK=w647-h910-no"></a>
	<figcaption><center>Verilog diagrams</center></figcaption>
</figure>


<figure class="half">
	<a href="https://lh3.googleusercontent.com/MuYXZOu6qxx_09Jj_FnZt1uMygpljiKU_yfVAqg3E44NQV2IB2hEbf66BMrRpEVaNwRKvyl6SesjKJORO-Qd6_0cf6OUhyQYYA8gLmaaYuA6vZTOmFZu2SJMbfpMr72RKf_w6bqZjrvkYho4zlMnusov7ZpxLPrXEwA52Kd8hZQXxxE7KprIcbfDXWZJjb9Pz0adGK6ZRwmp8pDkP47c0dTWJCH3EOT9P66yJK7Hwa_34RPXgQs3T1pkdzWyyGszKXQM7VJVQ1c9vLg_BLAC0QAHFTTlON7eRywnh8fOzxZbrzqZKkX0xvkzNUB74tLQMaYqZCg91aCgYFZA97PvUf5fVpo_3kuYdynz5GZ91e1wpk_L0mA5A4zJAGFl_crbh6RKdDtSWfdhYENm-ujcVG33KNGPNgvPXYgpuUCRouf6W_CCD41aQLBwtG9ysRWPYO4RToS-_LcTtiCwg-ffeHCnlJIBOc8h5GS2bv-tDnvMZ61--hJ41rgEoWrfg8n7GkALERzBUd-cimVhTQuVCnqiyuGouJiE1JJNJHnKDff2LLmrUyNYEEzC9f89NqpqC-38o1NU0AKsxbs4ZNj9wRHAFE2cZwS8uQs-B_55S6TZTDvkE0DdWKcey1nSH0HvirJSbx2ImtfAv4t42_UTtZ8xnmwp9rbE=w1100-h825-no"><img src="https://lh3.googleusercontent.com/MuYXZOu6qxx_09Jj_FnZt1uMygpljiKU_yfVAqg3E44NQV2IB2hEbf66BMrRpEVaNwRKvyl6SesjKJORO-Qd6_0cf6OUhyQYYA8gLmaaYuA6vZTOmFZu2SJMbfpMr72RKf_w6bqZjrvkYho4zlMnusov7ZpxLPrXEwA52Kd8hZQXxxE7KprIcbfDXWZJjb9Pz0adGK6ZRwmp8pDkP47c0dTWJCH3EOT9P66yJK7Hwa_34RPXgQs3T1pkdzWyyGszKXQM7VJVQ1c9vLg_BLAC0QAHFTTlON7eRywnh8fOzxZbrzqZKkX0xvkzNUB74tLQMaYqZCg91aCgYFZA97PvUf5fVpo_3kuYdynz5GZ91e1wpk_L0mA5A4zJAGFl_crbh6RKdDtSWfdhYENm-ujcVG33KNGPNgvPXYgpuUCRouf6W_CCD41aQLBwtG9ysRWPYO4RToS-_LcTtiCwg-ffeHCnlJIBOc8h5GS2bv-tDnvMZ61--hJ41rgEoWrfg8n7GkALERzBUd-cimVhTQuVCnqiyuGouJiE1JJNJHnKDff2LLmrUyNYEEzC9f89NqpqC-38o1NU0AKsxbs4ZNj9wRHAFE2cZwS8uQs-B_55S6TZTDvkE0DdWKcey1nSH0HvirJSbx2ImtfAv4t42_UTtZ8xnmwp9rbE=w1100-h825-no"></a>
	<a href="https://lh3.googleusercontent.com/xjyB6zcqnyTDj_gnDEwwM21bbi_539vmY9fatMmGkhKQIXNnmoYikMU8QUojXtXBpkcUJf44n278lBDfQDFwZPV8QvCyLYMS8uFwy4b8u_BauhRLGPjvca-l8HG0RUtM2Vl4WqOfutUrnzRXLdg0STBbvc9_JHnzJsJNXvAc-uTR4Tt23m07M0asRxD4RaELMBvKvUV01B8kQwI2xT1XqYj8MBBjWkJbqmNFpMJc1ZTJpfvHas5eNjebMvIvcm3Ja1eT-wxq55QG4ZBwdGHvjWlRFaH6MhEV9qvU-6JJXQPE48uP_fgwi2Isrg1CxPYp8i8DVJzySqnFcsb2NaJcqfkie0YzVaptuePvrsHvhYM_oTNmcpcySFEG5DqA3wvMB3e07jwFPPKiB57MXNugLIayyE4FRKMXCL2uWcHDzVP-U8rOZojzGdEvxGTQLMDkf5ITjiv1KDczny7eUVJGsKPUMbcqadwrDYpjeTbb8KKV8-1JwloL99bB-rR9eVYAPN0JZ9RKX3fjTSP_Ol7wSLKhL_lNP37kzq546Lea9Nh1MHQSNKfUeWB21WLz0dWn4C5hN8Z_hPm66myavsC2rOpqhgLc9iQyRFP6FC7BdWdb1P3iDUQzVXuuofDjANzIRvXk5zEnpDiFzCEZmlIoSFrF0eEzAlxT=w300-h225-no"><img src="https://lh3.googleusercontent.com/xjyB6zcqnyTDj_gnDEwwM21bbi_539vmY9fatMmGkhKQIXNnmoYikMU8QUojXtXBpkcUJf44n278lBDfQDFwZPV8QvCyLYMS8uFwy4b8u_BauhRLGPjvca-l8HG0RUtM2Vl4WqOfutUrnzRXLdg0STBbvc9_JHnzJsJNXvAc-uTR4Tt23m07M0asRxD4RaELMBvKvUV01B8kQwI2xT1XqYj8MBBjWkJbqmNFpMJc1ZTJpfvHas5eNjebMvIvcm3Ja1eT-wxq55QG4ZBwdGHvjWlRFaH6MhEV9qvU-6JJXQPE48uP_fgwi2Isrg1CxPYp8i8DVJzySqnFcsb2NaJcqfkie0YzVaptuePvrsHvhYM_oTNmcpcySFEG5DqA3wvMB3e07jwFPPKiB57MXNugLIayyE4FRKMXCL2uWcHDzVP-U8rOZojzGdEvxGTQLMDkf5ITjiv1KDczny7eUVJGsKPUMbcqadwrDYpjeTbb8KKV8-1JwloL99bB-rR9eVYAPN0JZ9RKX3fjTSP_Ol7wSLKhL_lNP37kzq546Lea9Nh1MHQSNKfUeWB21WLz0dWn4C5hN8Z_hPm66myavsC2rOpqhgLc9iQyRFP6FC7BdWdb1P3iDUQzVXuuofDjANzIRvXk5zEnpDiFzCEZmlIoSFrF0eEzAlxT=w300-h225-no"></a>
	<figcaption><center>In game screenshots</center></figcaption>
</figure>

You can find the code here: <a href="https://github.com/mpekatsoula/Acl_pong/">https://github.com/mpekatsoula/Acl_pong/</a>