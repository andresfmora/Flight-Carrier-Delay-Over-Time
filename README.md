# Summary
The Carrier Delay visualization shows us, on average, how many minutes of departure delay can be attributed to a flight carrier over time. We can observe cyclical and long term trends as well as how flight carriers compare to each other. The Legend is interactive which lets us focus in on particular airlines one at a time. You will also find a linear regression line of the overall data-set which highlights the overall trend of the data over time. 

This project also let me apply some tools I have been wanting to learn/try such as D3/Dimple for interactive web visualiztion, sklearn for a simple regression problem, and github pages to host a HTML page.

Link to interactive chart hosted on github pages

<https://andresfmora.github.io/>

# Design 
One of the key area of focus was to ensure that the X axis, which contains timestamp data,  displayed as it should. When I initially displayed the visualization using dimple, the x axis tick marks were completely unreadable due to the frequency of the tick marks and the formatting of the dates. This was fixed by using dimples timePeriod and timeInterval functionality. My axis now show in a readable and consistent format with a tick for every six months. Reflecting back, this change was one the hardest and took the longest to figure out as I had a lot of trouble to get dimple to read the date-format as it should. I had to go through a lot of dimple and D3 documentation in order to finally make it work.

One of the nice things about dimple is that fact that it has interactivity built in straight out of the box so the fact that tooltips were already implemented was nice as this is  something I would have added otherwise as it really contributes to being able to explore the data underneath the visualization. 

Another area of focus was the legend. This was a very important part of this visualization as there are many different airline carries that I wanted to display. 

The first aspect of the legend that had to be adjusted was the positioning. With standard dimple settings, the legend was too large and would simply not fit or be readable. In order to fix this I had to adjust the positioning of the legend as well as the size. This was done by adjusting the parameters on the addLegend functionality in dimple until I was happy with the layout and size of the legend.

**Visualization with Legend**

![View of Legend Positioning](https://lh3.googleusercontent.com/my4vroMv7QFbHgvi2_fOjsrLvtooEK_2TGWfjUXSVxAagcAaKxX3lYZBL1sRYG5lL6nFhZ_bJw3PgA "Full Visualization")

The second aspect of the legend that had to be improved, as was found out during the feedback process, was to add interactive functionality in order to highlight/filter specific airlines. I was able to look up a an example of interactive legends in the advanced examples sections of the Dimple.JS website. I was able to use code in this example and make it work for my visualization after extensive tweaking. 

**Top 3 Carriers Highlighted**

![enter image description here](https://lh3.googleusercontent.com/HrtK1Whp_tHLI56J00eKfpbMvcVEP1sKGgVJsV5-52yvlwHdSyHD55-b9BuTflO-OrlCR1SSZ2XFZA "Top 3 Airline Carriers")

This greatly improves the usability/impact of the visualization as one can now highlight just one airline and compare its trend to the linear regression for example. 

**American Airlines vs Regression**

![enter image description here](https://lh3.googleusercontent.com/82U5tOmI2RbDnXQXywsLIbP0KlO9AJhr8WjTSAZ9JtQE8CigK5GKFM1XY1nM9bw5SBL_grQSlhTltQ "Regression")

**Final Graphic**

![enter image description here](https://lh3.googleusercontent.com/LL11QqBIfKyj5kB5qZzGxFxqQ5kSG2rPUtd8QFOV5kHdkihR_qwRBZ9mi3uMCudYjYHN-k-QJf_5RA "Final")

# Resources 
- http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends
- https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.axis#timePeriod
- https://github.com/d3/d3-time/blob/master/README.md#timeInterval
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjc1NzIwNjU5LC0xMDg1NTkwMzQyLDIwOD
I1NDYwMDZdfQ==
-->
