---
title       : SCARA Manipulation App
subtitle    : Developing Data Products Project
author      : Luis Martin Alonso
job         : Attending Coursera and JHU Data Science Specialization
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## SCARA

- Selective Compliance Assembly Robot Arm or Selective Compliance Articulated Robot Arm
- Very simple robot, but very useful
- A good introduction for beginners in robotics

--- .class #id 

## SCARA App

- Allows changing the physical parameters (links length)
- Allows manipulation of the rotational position of the links
- Displays the position of the links in a graph and the final position coordinates of the robot

---

## Code

- Based on Direct Kinematics
- Use the Rotation Angle of each link to determine the position
- Example


```r
L1=10;L2=5;angle_1=180;angle_2=90;
y<-L1*sin((angle_1)*pi/180)+L2*sin((angle_1+angle_2)*pi/180)
x<-L1*cos((angle_1)*pi/180)+L2*cos((angle_1+angle_2)*pi/180)
round(c(x,y),3)
```

```
## [1] -10  -5
```

Use the SCARA app to prove the answer in this slide: https://lmalonso.shinyapps.io/ShinyApp1

---

## Credits

- R. Caffo, J. Leek, and R. Peng for the Data Science Specialization
- Ramnath Vaidyanathan for Slidify
- RStudio team
- R Development Core Team
- R Packages developers
