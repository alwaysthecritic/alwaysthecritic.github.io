---
layout: post
title: "Experimenting with Octopress"
date: 2013-10-11 10:52
comments: true
categories: News
---

Installed and up and running on Github in about 10 minutes. Colour me impressed.

Now for some code:

``` scala Outputting a list of robots, one per line
object OutputGenerator {
    
    // Given a list of Robots, generate String in the output format required, one line per Robot.
    def render(robots: Seq[Robot]): String = {
        val lines = robots.map {
            case HappyRobot(x, y, facing) => "%d %d %s".format(x, y, facing)
            case LostRobot(x, y, facing) => "%d %d %s LOST".format(x, y, facing)
        }
        lines.mkString("\r\n")
    }
}
```