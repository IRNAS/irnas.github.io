---
layout: post
title: "Logarithm calculation in integer only system"
description: "Logarithm calculation for nodemcu integer for ES8266"
category: 
tags: []
---
{% include JB/setup %}

Common and useful practice for visually displaying measurements with a large dynamic range is by using base 10 logarithms, which are widely available in most systems. However to conserve space on ESP8266 modules with nodemcu LuA firmware, this operation is unavailable. 

We are introducing two methods, one calculating the logarithm using only basic operation and the other using a simple look-up table, taking the input value x in the range of 0 to 1023, since calculations and lookup are iterative, calculation time depends on the value. Each function has been benchmarked for values 1 and 1000. Since these LUA functions are not compiled, their length is simply the number of characters in text. Code is available on [GitHub](https://github.com/IRNAS/SimpleArduinoESP-Lua/blob/master/lua/led.lua).

 * function log_approx(x) using calculation approach: 492us for x=1000 and 221us for x=1, 325 characters long
 * function log_approx2(x) using lookup approach: 433us for x=1000 and 195us for x=1, 332 characters long
 
For the given length, both functions have very similar performance in timing and lengths, calculation approach being slower but smaller and lookup approach being faster but larger. Full details on the mathematical operation of these functions and reasoning behind them is present in the note [Implementation of Logarithmic Calculation Using Integer
Arithmetic on LUA without libraries]({{ site.url }}/downloads/logApprox/logApprox.pdf). The plot below shows the approximated values in integer arithmetic and the continuous values. 

![log approximation]({{ site.url }}/downloads/logApprox/f5.png)