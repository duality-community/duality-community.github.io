---
layout: post
title:  Making Variables Visible in Inspector
date:   2017-09-03
categories: Tips&Tricks
tags: inspector code beginner
excerpt:
mathjax: false
author: BaconGamer88
---

Beginner programmers in Duality may have begun to create their scripts, only to wonder why they can't read/write variables in the 
inspector. In Unity, you would declare the variable as public or put `[SerializeField]` in front of the variable. However, both approaches 
will not work in Duality. So how would you go about doing this? Well, this snippet shows how to do this with a float variable, but it will 
work with any variable type, including integers, strings and booleans.
```csharp
public class EpicScript : Component
{
    // Declare a field to actually store data in
    private float epicValue = 17.0f;

    // Declare a property to access it for reading and writing.
    // The editor will use this in the Object Inspector.
    public float epicValue
    {
        get { return this.epicValue; }
        set { this.epicValue = value; }
    }
    // Insert following code here.
```
This code tells the inspector to allow the user to modify/read the variable through the inspector and then gets the value set in the
inspector before the variable is used.
