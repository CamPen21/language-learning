# Adapter Pattern Exercise

## Problem Description

You are working on a media player application. The application can play mp3 files by default. You have a legacy module that can play mp4 and vlc files but it has a different interface.

Your task is to implement the Adapter Pattern to allow your media player to use the legacy module and play mp4 and vlc files.

## Instructions

1. Define a `MediaPlayer` interface with a method `play`.

2. Implement a `AudioPlayer` class that can play mp3 files and uses the `MediaPlayer` interface.

3. Define a `AdvancedMediaPlayer` interface with methods to `playVlc` and `playMp4`.

4. Implement a `LegacyMediaPlayer` class that can play vlc and mp4 files and uses the `AdvancedMediaPlayer` interface.

5. Implement a `MediaAdapter` class that adapts the `LegacyMediaPlayer` to the `MediaPlayer` interface. It should delegate the `play` call to the appropriate method of `LegacyMediaPlayer`.

6. Modify the `AudioPlayer` class to use the `MediaAdapter` when it needs to play vlc or mp4 files.

## Tips

- The `MediaAdapter` should check the audio type and call the appropriate method of `LegacyMediaPlayer`.

## Expected Output

You should be able to create an `AudioPlayer` and use it to play mp3, mp4, and vlc files. For example:

```python
audio_player = AudioPlayer()

audio_player.play("mp3", "beyond_the_horizon.mp3")
audio_player.play("mp4", "alone.mp4")
audio_player.play("vlc", "far_far_away.vlc")
audio_player.play("avi", "mind_me.avi")
```
