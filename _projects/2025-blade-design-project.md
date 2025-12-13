---
layout: project
title: Wind Turbine Blade Design Project
description: Advanced CAD, MATLAB, and ANSYS Project
technologies: [SolidWorks, MATLAB, ANSYS, ChatGPT]
image: /assets/images/radio-machine-cad.jpg
---

## Project Overview

For this class project, I worked in a group of four where we were tasked with designing a set of three wind turbine blades that would generate the most power given a specific set of constraints. These contraints were as follows:

- max blade radius: 6 in (0.152 m)
- hub radius: 1 in
- max chord length: 2 in
- max rotational speed: ≤ 2000 rpm
- Reynolds-number range: 9.3×10³ to 2.1×10⁴ (based on 5–95% wind bounds)
- material limits: stiffness & tolerances of SLA-printed Accura 25

The purpose of this project was to enhance our understanding of the various phenomena that govern the performance of a wind turbine and other fluid/heat transfer devices.

## Design Process

We began the design process with a brainstorming session to decide what characteristics we wanted our blade to have. After some discussion, we decided that our blade should be able to generate high torque at a low tip-speed ratio (TSR, λ≈3) and Reynolds number (Re≈1.55×10⁴). Next, we computed a target rotational speed for our blade of ~900 RPM given these choices. 

With these values obtained, we then chose the specific airfoil that we would use as our blade cross-section. Ultimately, we decided on S1223 because it provides:

- exceptionally high lift (CL up to ~1.8–2.0)
- strong CL/CD in the low-Re regime
- gentle stall behavior
- geometry compatible with Accura 25 printing

Next, we wrote MATLAB program with the help of ChatGPT to create a parametric model of the blade based on the airfoil data and plotted the lift coefficient (CL) as a function of the angle-of-attack (α) for S1223 and NACA 4412 as a baseline:

! [Lift coefficient (CL) as a function of angle of attack (α) for S1223 and NACA 4412]({{ "/assets/images/clvsalpha.png" | relative_url }}){: .inline-image-r style="width: 400px"}

Then, we used optimal α (α=3°) from the S1223 airfoil data to determine the twist profile (β(r)) as a function of blade radius (r), resulting in:

r/R : 0.2 → 0.3 → 0.4 → 0.5 → 0.6 → 0.7 → 0.8 → 0.9
β : 55.0 → 43.8 → 35.6 → 29.6 → 25.0 → 21.5 → 18.8 → 16.5

Lastly, we utilized SolidWorks to create the 3D model of our blade with all of the values calculated above and had them printed.

## Testing Summary

To test our blades' performance, we ran an ANSYS Fluent simulation to see how it would actually perform under the conditions we optimized it for. 

## My Contribution








![Shaded rendering of earlier version]({{ "/assets/images/radio-machine.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

Nulla et magna urna. Morbi a ipsum sollicitudin, rhoncus risus volutpat, ultricies nunc. Quisque mollis finibus ante id imperdiet. Quisque vehicula elit sit amet felis facilisis fermentum.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

I was inspired by this old radio when I made this rendering:

![Photo of old radio]({{ "/assets/images/old-radio.jpg" | relative_url }}){: .inline-image-l}

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.
