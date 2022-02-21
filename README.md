## VLC mosaics for security cameras

### Overview
This repo contains .vlm files that are used to launch VLC mosaics via the Windows command line. Each mosaic is configured to display four rtsp streams (one per security camera). The .vlm files are identical except that each is configured for a different resolution (1080p, 1440p, and 2160p).

### Setup
Editing the .vlm files is straightforward, but at a minimum you will need to do the following:

 - Update `path_to_file` for the background image
 - Update each rtsp string to reflect the correct values for `admin`, `password`, `IPaddress`, and `channel`

### Launch
Launch a mosaic using the Windows command line. 

    vlc --vlm-conf path_to_file.vlm

Alternatively, launch using the -Idummy flag so that only one VLC window opens. In this case, the VLC window must be closed using Ctrl+Q (for some reason the [x] button doesn't work).

    vlc -Idummy --vlm-conf path_to_file.vlm

Audio volume can be controlled using the mouse scroll wheel within VLC.

The above commands must be run from the directory that contains `vlc.exe`. For VLC version 3.0.16, the default installation directory is `C:\Program Files\VideoLAN\VLC`.