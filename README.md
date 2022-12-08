# A Smart Control of Room Temperature based on number of people using DGIStreamer
**Author**: *Bauyrzhan Zhakanov*, [bauyrzhan.zhakanov@gmail.com](bauyrzhan.zhakanov@gmail.com)

## Introduction
**Goal** a develop a system to control the temperature in a room based on the people inside based on DGIStreamer tool. All the rights for **CYENS**.

Plan for the first time is to build a connection between local and remote systems using DGIStreamer. This is possible with a help of SSH. It takes streaming video as input, counts the number of people crossing a tripwire and sends the live data to the cloud. 

The number of people can be counted with a help of OpenCV, Python3. The system could be connected through the same internet or Wifi. To control room temperature, the simple counting technique will be used. If a person or people crosses a particular line in a camera, then it would be considered as part of count. A person would be detected using the box of Human Detection Deep Learning techniques that would allow to recognise a person from image. If a box of person or boxes of people intersects with a particular line inside the frame, then it would be considered as part of count. For instance:

- if there is no people crossed the line, then 0 person

- if there is some people crossed the line, then +1 person
