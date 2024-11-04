# ffmpeg-tools

A A collection of bash scripts to make muting video files easier using `ffmpeg`.

Requires `ffmpeg` to be installed.

See also [my quick ffmpeg cheat sheet](https://gist.github.com/Orangestar12/a6593a093d8728a268a799ff9003d815)

# [`gifit`](gifit)

Converts a video into a gif file. Uses the simple method from [this guide](https://github.com/cyburgee/ffmpeg-guide).

Syntax:

```
gifit input.mp4 output.gif
```

If the output filename is not specified, then the output will be named `output.gif`.

# [`trim`](trim)

Trims a file into an MP4 clip.

Syntax:

```
trim SS OT filename.mp4
```

Where:
- SS is the seek time, which can be a number in seconds or a full MM:SS / HH:MM:SS timestamp, like 2:30 or 150.
- OT is the out time, which is the timestamp or total seconds in which the video ends. This is not the duration.
- filename.mp4 is the output filename.

You can omit either the output filename or the out time, or both.
- If the filename is omitted, the filename will be output.mp4
- If the out time is omitted, the out time will be undefined (which is to say, it will be the end of the video.)
