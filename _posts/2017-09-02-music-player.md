---
layout: post
title:  Playing music across multiple scenes
date:   2017-09-02
categories: Tips&Tricks
tags: audio code
excerpt:
mathjax: false
author: loeller
---

A common scenario, usually with jam entries is when you need to loop an audio file through the whole game. Since we don't want our music loop to restart on `Scene` changes, `Components` are out of the game here (*pun intended*). Insted, we might want to touch the otherwise not-very-popular `CorePlugin`, and make use of a recently introduced virtual method: `CorePlugin.OnGameStarting`.

```csharp
static class AudioPlayer
{
    public static void PlayMusic ()
    {
        // load the resource from the DATA folder
        ContentRef<Sound> musicRes = ContentProvider.RequestContent<Sound> (@"DATA\Audio\Music.Sound.res");
        // start playback
        SoundInstance musicInstance = DualityApp.Sound.PlaySound (musicRes);
        // set the returned SoundInstance to loop
        musicInstance.Looped = true;
    }
}

public class Duality_CorePlugin : CorePlugin
{
    protected override void OnGameStarting ()
    {
        // start music with the game
        AudioPlayer.PlayMusic ();
    }
}
```