# Face Alignment and Stabilization 

* Face Alignment and Stabilization - 10 FPS
  * [![](http://img.youtube.com/vi/w94oYYK-loI/0.jpg)](http://www.youtube.com/watch?v=w94oYYK-loI "Face Alignment and Stabilization - 10 FPS")



* Face Alignment and Stabilization - 15 FPS
  * [![](http://img.youtube.com/vi/ut5pQAaAMWU/0.jpg)](http://www.youtube.com/watch?v=ut5pQAaAMWU "Face Alignment and Stabilization - 15 FPS")



## Editing Video

- The input video obtained from the phone was higher resoultion. Used iMovie (Mac) to crop the region for the video. It's similar to cropping the image.



## Converting the Images to Video

- Using openCV method - it failed with below mentioned codec error.

  - openCV: FFMPEG: tag 0x5634504d/'MP4V' is not supported with codec id 12 and format 'mp4 / MP4 (MPEG-4 Part 14)'

    OpenCV: FFMPEG: fallback to use tag 0x7634706d/'mp4v'

- Used **ffmpeg** to generate the video.

  - List down all the name of the images in file - **file_paths.txt**

    - The **format** of the file is as follows.

      file './StitchedImages/stitch_0.png'
      file './StitchedImages/stitch_1.png'
      file './StitchedImages/stitch_2.png'
      file './StitchedImages/stitch_3.png'
      file './StitchedImages/stitch_4.png'
      file './StitchedImages/stitch_5.png'
      file './StitchedImages/stitch_6.png'

      ...

      

  - ffmpeg -y -r 10 -f concat -safe 0 -i "./file_paths.txt"  "out_fps10.mp4"

    - r is frames per second.
    - Concat - to stitch the images

- Uploaded the video to youtube.



## How to embed the video url in the markdown.

- Used <http://embedyoutube.org/> . Provide the youtube url and this website will generate the embed url, which can be used in the markdown.

