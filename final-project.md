# Final project

We had a team of 7 people create a "massive" **techno club** with an "on-the-spot" DJ, and a "large" dance floor with LED light effects. The LED lights would react to the crowd movements.
3 people would handle the sound creation, 2 people would handle the traingulation of the crowd and we would make the lights shine.


This is a sketch of our project made by one of our team:  
![Sketch of project](https://media.discordapp.net/attachments/1234801171366154283/1243994609877516449/iot.png?ex=666b3ac3&is=6669e943&hm=200251fe2d09db8a2512fba1a7c023cb7e686795cb4bb3e3cf973ba20535377e&=&format=webp&quality=lossless&width=693&height=482)


# Result

*We are only reporting on our part. For the other parts, check out their own reports.*  
The sound was awesome to hear, the way it worked was magical.  
The triangulation data was fairly accurate, and we recieved location data in a 3x3 matrix (in form of "how close is the node to the signals?")

Our part was to take that data and generate visual effects based on the location. We had one node and one LED panel (WS2812 strip snaked for a 8x8 square) connected to an external 5V power supply. Everything else was with code.  
We started the task with great enthusiasm, until we found out that the main library was broken at that time. The older one worked, so we used FastLED library to control the panel.  
Testing out the `led_matrix` set up was unsucessful, we could not figure out what was wrong with it. We abandoned the plan to use it with the lack of time.

For controlling the LEDs, we made a virtual display, which is just an 8x8 array matrix with every pixel's color values.
* Details to be added



Our first choice was to make a simple circle using the help of GPT (we don't remember much trigonometry):  
![Solid circle](https://media.discordapp.net/attachments/701128655547531286/1244736604501835806/rn_image_picker_lib_temp_a5c0c544-175a-4764-b41a-9fe11e4f881b.jpg?ex=666b4acc&is=6669f94c&hm=8c524e7440029e2ea9b4bdac900e68a4a9b477afdbb83d85911b65490ff4deb4&=&format=webp&width=361&height=481)

Then we expanded on that with an expanding circle:  
[Expanding circle (video)](https://imgur.com/a/eUkg2gA)

And after adding a background to the effects we were finished with the simple effects:  
[Final show (video)](https://imgur.com/a/o71ESPK)

* Dashboard features to be added


*Node-Red flow and Dashboard are not added due to us forgetting to take screenshots before giving away the laptop. Sorry :(*
