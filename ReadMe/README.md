# Summary
The Carrier Delay visualization shows us, on average, how many minutes of departure delay can be attributed to a flight carrier over time. We can observe cyclical and long term trends as well as how flight carriers compare to each other. The Legend is interactive which lets us focus in on particular airlines one at a time. You will also find a linear regression line of the overall data-set which highlights the overall trend of the data over time. 

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


# Feedback 
- Feedback Round 1: Jackie (Fiance)

I started collecting feedback from my Fiance starting with graph below. Her immediate feedback was that there were to many lines to makes sense of the data which makes it hard for you to follow one line or compare and contrast more than one line.

![enter image description here](https://lh3.googleusercontent.com/GJYFmnpEWpKD92d3gLYTF1_0oD-fbScIpd5JBRsjZz-mBeEthqKmv3epM3Q9a6164KJTuLRtaZ3bBQ "Round 1")

Based on this, I went ahead and added a interactive legend which lets you filter down and look at one or a few airlines at a time.

- Feedback Round 2: Brian(Friend)

After making updates to visualization based on round 1, I showed this visualization seen below to my friend Brian. He found it interesting but wished it was easier to see the over trend of the data as right now it looks like the airlines might be flat but hard to tell if there is an overall trend.

![enter image description here](https://lh3.googleusercontent.com/s_r5yW89mA77waKkcWo1nT5CKHE82XS9qKFIhhwZ5GLsdJ9hDiJ8sY28pit6Hrf6DuZ-jkixsLk1-g "Round 2")


Based on this feedback, I went back to my python data munging file and added a linear regression line on the full dataset using Sklearn. This line ends up adding a lot of context to the visualization as it highlights the overall upward trend of the data and also let's one see if an airline is generally above or below this best fit line. 
- Feedback Round 3: John (Co-Worker)

After adding the best fit line, I showed the visualization below to my coworker John. He liked the visualization but what became apparent is that it is not immediately obvious what it is you are looking at. It always took some time explaining what the visualization was showing. 

![enter image description here](https://lh3.googleusercontent.com/V6PF7j84hLJlLkipd9zOkMeDZ6Hucydgpu13-TigspSSnOwon_bfydpbqRkQujO7zE4IHiRzdtrq7Q "Round3")

Based on this I added a title a brief description of what the visualization is showing. I also used a bit of CSS in order to control color/font/size. 

- Final

After these rounds of feedback I am left with my final visualization shown below!

![enter image description here](https://lh3.googleusercontent.com/LL11QqBIfKyj5kB5qZzGxFxqQ5kSG2rPUtd8QFOV5kHdkihR_qwRBZ9mi3uMCudYjYHN-k-QJf_5RA "Final")

# Resources 
- http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends
- https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.axis#timePeriod
- https://github.com/d3/d3-time/blob/master/README.md#timeInterval
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjc1NzIwNjU5LC0xMDg1NTkwMzQyLDIwOD
I1NDYwMDZdfQ==
-->