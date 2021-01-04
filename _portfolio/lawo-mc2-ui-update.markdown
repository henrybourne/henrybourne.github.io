---
layout: portfolio
title:  "Lawo mc² UI Update"
launched: 2020
---

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/hero.jpg"></div>

Since joining Lawo in December 2019, I’ve been working hard to set up and integrate Experience & Design across the organisation. There’s been a lot happening. Today, I’m pleased to be able to discuss the first small steps of many good things to come.

The launch of the mc²36 MKII and phase 2 of the UHD Core development marks a significant step in Lawo’s audio production product line. I won’t go into detail here, but here are the links for the [mc²36](https://lawo.com/mc²36/) and the [A__UHD Core](https://lawo.com/a__uhd-core/) if you want to learn more.

Because of the significant improvements in product, performance, physical space, and power, we wanted to refresh the look and experience of using the mc² series products.

There are many constraints with this type of UI update to established and popular products. It requires careful balance to respect the functionality, workflows, and familiarity of the existing mc² UI for Lawo’s current customers, but to bring the appearance and workflows up to date with people’s expectations of a product in 2020.

The small first steps in this update outlined below. I’ll write more in future to highlight more areas that I think you’ll find interesting.


## Channel Display

The Channel Display is shown in the left-hand display on the surface.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/mc236-front.jpg"></div>

It presents strips of information above each fader on the surface. This information includes, amongst other things, the channel label, signal metering, bus routing, VCA group assignment, link assignment, automaker assignment, gain reduction meters, and a summary of channel processing.

You can choose which information is displayed in the strips to balance a clean and clear display with minimal information against a busier display if you need to see an overview of more information at once.

This allows at-a-glance understanding of a subset of important channel information, and the ability to quickly interact with it if required.

For reference, here is a detailed look at the previous Channel Display.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/channel-display-old.png"></div>

The issue here is that there is too much visual noise. Visual noise is stimuli received and interpreted by your eyes and brain, but which has limited or no useful information. The more information you need to process to understand what you’re looking at, the harder you need to work. If we can reduce the unnecessary information—the noise—we can help reduce the amount of work you need to do, and help you make easier and faster decisions.

In the channel display, there are a few big sources of noise:

### Bright Borders
The bright borders around each channel area. These are one of the brightest elements in this view and are one of the first things I notice. As they are single pixel lines with high contrast to the background, they create sharp edges. Edge detection is a crucial component of our visual system. The more sharp edges we see, the more we pay attention to them.


### High Visual Priority Given to Low Priority Information
Examples in this view are buses to which a channel is not routed, source settings such as 48V or low cut filters that are off, gain reduction meters for inactive dynamics processes. These are all examples of information that is given an undeservedly high visual priority, that they compete with more useful and important information such as the buses to which the channel is routed, or the dynamics process that are active.

### Mini Displays
The ‘Mini Display’ towards the bottom of the strip shows a small summary of a specific block of processing within a channel. It might show an EQ curve, the transfer function for a dynamics process, or a pan position. In this previous version it’s a sea of bright green lines, with the different views looking similar. It can be difficult to quickly see which process you are looking at, and what the current state or each block is. There’s too much noise.

Here’s the updated version following the UI update. There are a few differences in this screenshot from the one above, for example the row of buttons across the middle is not shown, but it covers the main points.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/channel-display-new.jpg"></div>

The main improvement that I hope you perceive is a greater sense of space and calm. It feels like there is more room to breath, and it’s easier to make sense of the information.

The bright and sharp borders between each channel section have been removed and replaced with a wider and less aggressive negative space. I find that this provides sufficient information to demarcate each area with much less noise.

Unimportant information has been de-emphasised so that it does not compete with important information. In the bus routing areas, the buses to which the channels are not routed are now much less prominent, and the buses to which the channels are routed are clearer. Gain reduction meters blend into the background when the appropriate dynamics processes are turned off, and spring forward when enabled.

The Mini Displays are colour coded to match the colours of the controls on the surface. This makes it quicker to understand what you’re looking at with a quick glance. Noise has been dramatically reduced by emphasising important information in each view, such as the EQ curve, transfer function, or pan position, and de-emphasising unimportant information such as unnecessarily bright lines on a graph.

In addition to these main points, there are lots of other smaller changes to colours, spacing, alignment, and architecture  that tighten up the view and make it easier to parse and understand.

## Main Display

The Main Display is shown in the right-hand display on the surface.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/mc236-front.jpg"></div>

It provides access to detailed control of all parameters of the selected channel. It’s a dense view, with lots of different information competing for attention, but it’s important and used frequently.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/main-display-old.png"></div>

The main points of interest for improvement here are:

### Noise
As with the Channel Display, there are instances of high visual noise. These include the bright borders around buttons, meters, and faders, the bright green text in the input fields, the strong blue lines at the top of different areas, the colours in the background of the header, and the level of detail in the small icons throughout the view.

### Overuse of Colour
There is lot of green. The majority of buttons in this version are coloured green when they are active—this is a theme’s default colour. The text in all input fields is green. As colour has specific meaning to certain functions or states in the system, an overuse of colour in inappropriate places can cause confusion, de-emphasis, and noise.

Here’s the updated Main Display.

<div class="post-image"><img src="/assets/images/portfolio/lawo-mc2-ui-update/main-display-new.jpg"></div>

As with the Channel Display, the view has been tweaked for better use of colour, spacing, alignment, and architecture, which provides more breathing room and makes it all easier to parse.

The amount of visual noise has been reduced by removing sharp borders and edges, and updating interface elements like buttons, input fields, and faders, so that they provide

Colour has been reduced but retained when appropriate. Button colours in the touch screen UI now match with button colours on the physical surface. As colour can be used as an indicator of state, or as an indication of control type, it’s important to maintain consistency between surface LED colours and screen UI colours. For example, surface buttons that turn on and off different channel processes such as dynamics and EQ illuminate white when the process is on. This is now reflected in the screen UI. The colour of the screen UI graphs and illustrations of the processing blocks now matches the colour of the controls on the surface.

## A First Small Step
As I mentioned at the start, this is just an initial small delivery and there’s lots more to look forward to. Whether you like these changes or not, I hope you’ll get in touch and pass on your thoughts so that we can continue to improve.
